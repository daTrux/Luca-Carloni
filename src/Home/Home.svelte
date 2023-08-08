<script>
  let logo = "assets/Logo.jpg";
  let profile = "assets/PT.jpg";
</script>

<section id="home">
  <div class="img-div">
    <img src={logo}>
  </div>
  <div class="img-div profile">
    <img src={profile}>
  </div>
  <h1 class="title">Lorem ipsum dolor sit amet</h1>
</section>

<style>
 
 
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
</style>
