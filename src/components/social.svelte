<script lang="ts">
  const name2icon = new Map<string, string>([
    ["GitHub", "src/assets/imgs/github.svg"],
    ["Discord", "src/assets/imgs/discord.svg"],
    ["Telegram", "src/assets/imgs/telegram.svg"],
    ["Mail", "src/assets/imgs/maildotru.svg"],
  ]);

  export let social: string;
  let icon = name2icon.get(social);
</script>

<img src={icon} alt="Product icon of {social}" />

<style>
  img {
    height: 1.88rem;
    width: auto;
  }
</style>
