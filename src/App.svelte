<script>
  import Navbar from "./Navbar/Navbar.svelte";
  import Home from "./Home/Home.svelte";
  import Contacts from "./Contacts/Contacts.svelte";
  import About from "./About/About.svelte";
  import Structure from "./Structure/Structure.svelte";
  import "@splidejs/svelte-splide/css/splide.min.css";
</script>

<div id="navbar">
  <Navbar />
</div>
<div id="main-content">
  <Home />
  <About />
  <Structure />
  <Contacts />
</div>

<style>
  #navbar {
    display: block;
  }
  #main-content {
    padding-top: 50px;
  }
</style>
