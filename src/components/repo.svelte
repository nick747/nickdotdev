<script lang="ts">
  import { onMount } from "svelte";

  export let index: any;
  let name: string = "";
  let description: string = "";
  let language: string = "";
  let url: string = "";
  let topics: string[] = [];
  index = parseInt(index);

  onMount(async () => {
    try {
      const result = await fetch(
        "https://api.github.com/users/nick747/repos?sort=updated_at",
      );
      let data = await result.json();
      data = data.filter((repo: any) => repo.fork !== true);

      if (data.length > index) {
        name = data[index].name || "";
        description = data[index].description || "";
        language = data[index].language || "";
        url = data[index].html_url || "";
        topics = data[index].topics || [];
      }
    } catch (error) {
      console.error(error);
    }
  });
</script>

<div class="repo">
  <div class="info">
    {#if name}
      <span id="name">{name}</span>
    {/if}
    {#if description}
      <span id="description">{description}</span>
    {/if}
    {#if language}
      <span id="language">{language}</span>
    {/if}
  </div>

  <div class="topics"></div>

  {#if url}
    <a href={url} id="url" target="_blank">View on GitHub -></a>
  {/if}
</div>

<style>
  a {
    text-decoration: none;
    cursor: pointer;
    transition: all .3s ease;
  }

  .repo {
    min-height: 8rem;
    width: calc((100% / 3) - 2rem);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: rgba(54, 54, 54, 0.5);
    border: 1px #363636 solid;
    border-radius: 10px;
    padding: 2rem;
    filter: drop-shadow(0px 0px 10px rgba(0, 0, 0, 0.25));
    transition: all 0.3s ease;
  }

  .info {
    display: flex;
    flex-direction: column;
  }

  #name {
    font-size: 20px;
    font-weight: 700;
    margin-bottom: 1rem;
    transition: all 0.3s ease;
  }

  #description {
    font-size: 14px;
    font-weight: 400;
    margin-bottom: .5rem;
  }

  #language {
    font-size: 14px;
    font-weight: 500;
    color: rgba(255, 255, 255, 0.5);
  }

  #url {
    font-size: 14px;
    font-weight: 400;
    color: rgba(255, 255, 255, 0.5);
  }
</style>
