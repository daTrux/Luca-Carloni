<script>
  export let dialog;
  import { onMount } from "svelte";

  onMount(() => {
    // const alreadyClosed = localStorage.getItem("isPopupClosed");
    // if (!alreadyClosed) {
    //   dialog.open = true;
    // }
    dialog.open = true;
  });
</script>

<dialog bind:this={dialog} on:close>
  <slot />
</dialog>

<style>
  dialog {
    position: absolute;
    border-radius: 2px;
    max-width: 150px;
    bottom: 5px;
    left: -260px;
    padding: 0.5em;
    border: 1px white solid;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  }
</style>
