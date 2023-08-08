<script>
  export let dialog;
  import { onMount } from "svelte";

  onMount(() => {
    const alreadyClosed = localStorage.getItem("isPopupClosed");
    if (!alreadyClosed) {
      dialog.open = true;
    }
  });
</script>

<dialog bind:this={dialog} on:close>
  <slot />
</dialog>

<style>
  dialog {
    position: absolute;
    max-width: 150px;
    bottom: 5px;
    left: -260px;
  }
</style>
