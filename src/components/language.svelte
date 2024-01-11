<!-- Badge for the languages in the about section -->

<script lang="ts">
  let languages = new Map<string, string>([
    ["HTML", "src/assets/imgs/HTML.svg"],
    ["CSS", "src/assets/imgs/CSS.svg"],
    ["JavaScript", "src/assets/imgs/JavaScript.svg"],
    ["React", "src/assets/imgs/React-Dark.svg"],
    ["Svelte", "src/assets/imgs/Svelte.svg"],
    ["TailwindCSS", "src/assets/imgs/TailwindCSS-Dark.svg"],
    ["Astro", "src/assets/imgs/Astro.svg"],
    ["Flutter", "src/assets/imgs/Flutter-Dark.svg"],
    ["Dart", "src/assets/imgs/Dart-Dark.svg"],
    ["C", "src/assets/imgs/C.svg"],
    ["CPP", "src/assets/imgs/CPP.svg"],
    ["VSCode", "src/assets/imgs/VSCode-Dark.svg"],
    ["NeoVim", "src/assets/imgs/NeoVim-Dark.svg"],
    ["Python", "src/assets/imgs/Python-Dark.svg"],
    ["Kotlin", "src/assets/imgs/Kotlin-Dark.svg"],
  ]);

  let links = new Map<string, string | null>([
    ["HTML", null],
    ["CSS", null],
    ["JavaScript", null],
    ["React", "https://react.dev/"],
    ["Svelte", "https://svelte.dev/"],
    ["TailwindCSS", "https://tailwindcss.com/"],
    ["Astro", "https://astro.build/"],
    ["Flutter", "https://flutter.dev/"],
    ["Dart", null],
    ["C", null],
    ["CPP", null],
    ["VSCode", null],
    ["NeoVim", null],
    ["Python", null],
    ["Kotlin", null],
  ]);

  export let language: string;
  const imgSrc = languages.get(language);
  const imgUrl = links.get(language);
</script>

{#if imgUrl}
  <div
    class="language clickable"
    on:click={() => {
      window.open(imgUrl, "_blank");
    }}
  >
    <img src={imgSrc} alt={"Product icon of " + language} />
    <p>{language}</p>
  </div>
{:else}
  <div class="language">
    <img src={imgSrc} alt={"Product icon of " + language} />
    <p>{language}</p>
  </div>
{/if}

<style>
  .language {
    display: inline-flex;
    align-items: center;
    gap: 0.25rem;
    border-radius: 0.5rem;
    border: 1px #363636 solid;
    background-color: #242424;
    padding: 0.25rem;
    font-size: 0.875rem;
    line-height: 1.25;
    color: #1a202c;
    text-decoration: none;
  }

  .clickable {
    cursor: pointer;
    border: 1px #404040 solid;
    background-color: #303030;
  }
  img {
    height: 18px;
    aspect-ratio: 1;
  }

  p {
    font-size: 18px;
    font-weight: 500;
  }
</style>
