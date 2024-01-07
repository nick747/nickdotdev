<script lang="ts">
    import Repo from "./repo.svelte";
</script>

<div class="projects">
  <h2>Latest Projects</h2>
  <div class="cards">
    <Repo index="0"/>
    <Repo index="1"/>
    <Repo index="2"/>
  </div>
</div>

<style>
  h2 {
    font-size: 40px;
    font-weight: 600;
    margin-bottom: 1rem;
  }

  .cards {
    display: flex;
    width: 100%;
    justify-content: space-between;
    gap: 3rem;
  }
</style>