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

  export let language: string;
  const imgUrl = languages.get(language);
</script>

<div class="language">
  <img src={imgUrl} alt={"Product icon of " + language} />
  <p>{language}</p>
</div>

<style>
  .language {
    display: inline-flex;
    align-items: center;
    gap: 0.25rem;
    border-radius: .5rem;
    border: 1px #363636 solid;
    background-color: #242424;
    padding: .25rem;
    font-size: 0.875rem;
    line-height: 1.25;
    color: #1a202c;
    text-decoration: none;
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
