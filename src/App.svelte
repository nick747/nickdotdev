<script lang="ts">
    import About from "./components/About.svelte";
</script>

<main>
  <div class="main-info">
    <h1>NICK747</h1>
    <span id="role">teenager & developer</span>
  </div>
  <About />
</main>

<style>
  main {
    width: 80rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .main-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 5rem;
  }

  h1 {
    font-size: 96px;
    font-weight: 800;
  }

  #role {
    opacity: 0.5;
  }
</style>
