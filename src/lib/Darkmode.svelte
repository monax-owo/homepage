<script lang="ts">
  import { onMount } from "svelte";

  onMount(()=> {
    export const darkmode: boolean = 
  })
  const toggleDarkmode = (): void => {
    if (document.cookie) {
      
    }
  };
</script>

<div>
  <button
    on:click="{() => {
      toggleDarkmode;
    }}"
  >
    Toggle {#if darkmode}
      Light mode
    {:else}
      Dark mode
    {/if}
  </button>
</div>
