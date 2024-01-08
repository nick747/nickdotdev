<script lang="ts">
  const icons = new Map<string, string>([
    ["GitHub", "src/assets/imgs/github.svg"],
    ["Discord", "src/assets/imgs/discord.svg"],
    ["Telegram", "src/assets/imgs/telegram.svg"],
    ["Mail", "src/assets/imgs/maildotru.svg"],
  ]);

  export let social: string;
  const icon = icons.get(social);
</script>

<img src={icon} alt="Product icon of {social}" />

<style>
  img {
    height: 1.88rem;
    width: auto;
  }
</style>
