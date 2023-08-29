<script>
  let logo = "assets/Logo.jpg";
  let profile = "assets/PT.jpg";
</script>

<section id="home">
  <h1 class="title">Luca Carloni</h1>
  <div class="img-div profile">
    <img src={profile} />
  </div>
  <!-- <h2 class="description">
    LEZIONI DI PERSONAL TRAINING INDIVIDUALI E DI COPPIA
  </h2>
  <ul>
    <li>Bodybuilding</li>
    <li>Ricomposizione corporea</li>
    <li>Dimagrimento</li>
    <li>Riabilitazione e riatletizzazione</li>
    <li>Funzionale</li>
    <li>Ginnastica posturale e correttiva</li>
  </ul> -->
</section>

<style>
  @import url("https://fonts.cdnfonts.com/css/audrey");

  #home {
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
    max-width: 100vw;
    /* background-color: #ccc; */
  }
  .img-div {
    max-width: 100%;
    height: auto;
    margin-bottom: 2rem;
  }
  .img-div.profile {
    max-width: 50%;
  }
  .img-div.profile img {
    border-radius: 50%;
  }
  img {
    max-width: 100%;
  }
  .title {
    font-size: 4em;
    font-family: "Audrey";
    font-weight: 400;
  }
</style>
