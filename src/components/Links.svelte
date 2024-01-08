<script lang="ts">
  import Icon from "./social.svelte";
</script>

<div class="links">
  <h2>Links & Contacts</h2>
  <div class="icon_name">
    <div class="social clickable" on:click={() => window.open("https://github.com/nick747", "_blank")}>
      <Icon social="GitHub" />
      <span>nick747</span>
    </div>
    <div class="social">
      <Icon social="Discord" />
      <span>.mdotdev</span>
    </div>
    <div class="social clickable" on:click={() => window.open("https://t.me/nickodon", "_blank")}>
      <Icon social="Telegram" />
      <span>@nickdon</span>
    </div>
    <div class="social">
      <Icon social="Mail" />
      <span>nickodon747@proton.me</span>
    </div>
  </div>
  <p>
    This is my first project with Svelte, you can find the GitHub repo <a href="https://github.com/nick747/nickdotdev" target="_blank">here</a>.
    Feel free to give any suggestions!
  </p>
</div>

<style>
  .links {
    display: flex;
    flex-direction: column;
  }

  h2 {
    font-size: 40px;
    font-weight: 600;
    margin-bottom: 2.5rem;
  }

  .icon_name {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .social {
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  span {
    font-size: 18px;
    font-weight: 700;
  }

  p {
    margin-top: 2rem;
    font-size: 18px;
  }

  .clickable {
    cursor: pointer;
  }
</style>
