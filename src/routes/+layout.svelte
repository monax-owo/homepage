<script lang="ts">
  import "@csstools/normalize.css";
  import "@fontsource/zen-maru-gothic";
</script>

<div class="slot">
  <slot />
</div>

<style>
  :root {
    --bg: #e1e1e1;
  }
  * {
    background-color: var(--bg);
  }
</style>
