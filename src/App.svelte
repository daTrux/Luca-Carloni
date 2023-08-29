<script>
  import Navbar from "./Navbar/Navbar.svelte";
  import Home from "./Home/Home.svelte";
  import Contacts from "./Contacts/Contacts.svelte";
  import About from "./About/About.svelte";
  import Structure from "./Structure/Structure.svelte";
  import Footer from "./Footer/Footer.svelte";
  import "@splidejs/svelte-splide/css/splide.min.css";
  import Fab from "./ContactButton/ContactButton.svelte";
</script>

<div id="navbar">
  <Navbar />
</div>
<div id="main-content">
  <Home />
  <About />
  <Structure />
  <Fab />
</div>
<Footer />

<style>
  #navbar {
    display: block;
  }
  #main-content {
    padding: 8px;
    padding-top: 50px;
  }
</style>
