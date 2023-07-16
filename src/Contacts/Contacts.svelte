<script>
  import Fa from "svelte-fa";
  import { faEnvelope, faPhone } from "@fortawesome/free-solid-svg-icons";
  import { faWhatsapp } from "@fortawesome/free-brands-svg-icons";

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
</script>

<section id="contacts">
  <h5>Contattami</h5>
  <h1>Contattami in modo semplice tramite:</h1>
  <div class="contact-buttons">
    <div class="contact-icon" on:click={onEmail}>
      <Fa icon={faEnvelope} />
      <p>Email</p>
    </div>
    <div class="contact-icon" on:click={onPhoneClick}>
      <Fa icon={faPhone} />
      <p>Telefono</p>
    </div>
    <div class="contact-icon" on:click={onWhatsappClick}>
      <Fa icon={faWhatsapp} />
      <p>Whatsapp</p>
    </div>
  </div>
</section>

<style>
  #contacts {
    margin-left: 1rem;
    margin-right: 1rem;
  }
  h1,
  h5 {
    margin-block-start: 0;
    margin-block-end: 0;
  }
  h5 {
    margin-top: 1rem;
  }

  .contact-buttons {
    display: flex;
    justify-content: space-evenly;
    margin-top: 1rem;
  }
  .contact-icon {
    display: flex;
    flex-direction: column;
    justify-content: center;
    cursor: pointer;
  }
</style>
