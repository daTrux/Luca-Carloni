<script>
  import Fa from "svelte-fa";
  import {
    faPersonWalking,
    faAppleWhole,
    faBuildingCircleCheck,
    faDumbbell,
  } from "@fortawesome/free-solid-svg-icons";
  import Carousel from "../Carousel/Carousel.svelte";
  import Youtube from "svelte-youtube-embed";
  const spaceBetween = 10;
  const onProgress = (e) => {
    const [swiper, progress] = e.detail;
    console.log(progress);
  };
  const onSlideChange = (e) => {
    console.log("slide changed");
  };
</script>

<section id="services">
  <h5>I miei servizi</h5>
  <h1>Lezioni di personal training individuale o di coppia</h1>
  <ul>
    <li>Bodybuilding</li>
    <li>Ricomposizione corporea</li>
    <li>Dimagrimento</li>
    <li>Riabilitazione e riatletizzazione</li>
    <li>Funzionale</li>
    <li>Ginnastica posturale e correttiva</li>
  </ul>
</section>

<Carousel />
<section id="structure">
  <h5>La struttura</h5>
  <h1>Scopri Askesis Lab</h1>
  <p style="padding-bottom: 0.5rem">
    Askesis Lab è una struttura di 250 mq che fornisce solo ed esclusivamente
    servizio di personal training individuale o di coppia, estremamente
    specifico e programmato in funzione alle esigenze del nostro cliente. La
    sala pesi e quella funzionale sono allestite con macchinari isotonici,
    cardio ed accessori di ultimissima generazione: il tutto in un ambiente
    riservato e molto luminoso.
  </p>

  <Youtube id="K4TOrB7at0Y" />
</section>

<style>
  #structure {
    margin-left: 1rem;
    margin-right: 1rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
  }
  #services {
    margin-left: 1rem;
    margin-right: 1rem;
    padding-top: 1rem;
  }

  .list-item {
    display: flex;
    align-items: center;
    justify-content: start;
  }
  .item-text {
    margin-left: 1rem;
  }

  h1,
  h5 {
    margin-block-start: 0;
    margin-block-end: 0;
  }
  h5 {
    margin-top: 1rem;
  }
</style>
