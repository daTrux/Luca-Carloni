<script>
  let logo = "assets/Logo.jpg";
  let profile = "assets/PT.jpg";
</script>

<section id="home">
  <h1 class="title">Luca Carloni</h1>
  <div class="img-div profile">
    <img src={profile}>
  </div>
  <h2 class="description">Lorem ipsum dolor sit amet</h2>
</section>

<style>
 @import url('https://fonts.cdnfonts.com/css/audrey');
 
  #home {
    display: flex;
    flex-direction: column  ;
    justify-content: start;
    align-items: center;
    height: 100vh;
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
      font-family: 'Audrey';
      font-weight: 400;
    }
</style>
