<script>
  import Fa from "svelte-fa";
  import {
    faEnvelope,
    faPhone,
    faAddressCard,
    faMinus,
    faX,
  } from "@fortawesome/free-solid-svg-icons";
  import { faWhatsapp } from "@fortawesome/free-brands-svg-icons";
  import Dialog from "../Dialog/Dialog.svelte";

  let dialog;
  let isFabOpen = false;
  function toggleFab() {
    isFabOpen = !isFabOpen;
  }

  function onPhoneClick() {
    window.open("tel:3479183883");
  }

  function onEmail() {
    window.location.href =
      "mailto:luca.carloni.pt@gmail.com?subject=Primo%20Contatto&body=message%20goes%20here";
  }

  function onWhatsappClick() {
    window.open("https://api.whatsapp.com/send?phone=3479183883&text=Hello");
  }

  function closePopup() {
    dialog.close();
    // localStorage.setItem("isPopupClosed", true);
  }
</script>

<div class="fab-container">
  <Dialog bind:dialog>
    <div class="icon" on:click={closePopup}>
      <Fa icon={faX} />
    </div>
    <div><p>Clicca qui per contattarmi</p></div>
  </Dialog>
  <div class="fab {isFabOpen ? 'open' : ''}" on:click={toggleFab}>
    {#if isFabOpen}
      <Fa icon={faMinus} />
    {:else}
      <Fa icon={faAddressCard} />
    {/if}
  </div>
  {#if isFabOpen}
    <div class="fab" on:click={onPhoneClick}>
      <Fa icon={faPhone} />
    </div>
    <div class="fab" on:click={onWhatsappClick}>
      <Fa icon={faWhatsapp} />
    </div>
    <div class="fab" on:click={onEmail}>
      <Fa icon={faEnvelope} />
    </div>
  {/if}
</div>

<style>
  .fab-container {
    position: fixed;
    bottom: 0px;
    right: 5px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
  }

  .fab {
    width: 56px;
    height: 56px;
    background-color: #006879;
    color: whitesmoke;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 16px;
    cursor: pointer;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
    transition: background-color 0.2s;
  }

  .fab.open {
    background-color: #ff5722;
  }

  .sub-fab {
    width: 40px;
    height: 40px;
    background-color: #ff5722;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 8px;
    cursor: pointer;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25);
    transform: scale(0);
    transition: transform 0.2s;
  }

  .fab.open .sub-fab {
    transform: scale(1);
  }

  .icon {
    position: absolute;
    right: 5px;
    top: 5px;
  }
  p {
    margin-block-start: 0;
    margin-block-end: 0;
  }
</style>
