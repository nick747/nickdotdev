<script lang="ts">
  export let topic: string;
</script>

<div class="topic">
  <span>{topic}</span>
</div>

<style>
  .topic {
    min-width: 3rem;
    display: inline-flex;
    justify-content: center;
    gap: 0.25rem;
    border-radius: 1rem;
    border: 1px #363636 solid;
    background: rgba(54, 54, 54, 0.25);
    padding: .25rem .75rem;
    font-size: 0.875rem;
    line-height: 1.25;
    color: #1a202c;
    text-decoration: none;
  }

  span {
    font-size: 14px;
    font-weight: 500;
  }
</style>