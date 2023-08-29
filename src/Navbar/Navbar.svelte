<script>
  let showMenu = false;

  function toggleMenu() {
    showMenu = !showMenu;
  }

  function scrollToSection(event) {
    event.preventDefault();
    const targetId = event.target.getAttribute('href');
    const targetElement = document.querySelector(targetId);
    const offset = targetElement.offsetTop - 50;
    window.scrollTo({
      top: offset,
      behavior: 'smooth'
    });
    showMenu = false
  }
</script>

<nav>
  <div class="nav-container">
    <!-- <div class="logo">
      <img src="logo.png" alt="Apple Logo">
    </div> -->
    <div class="menu-toggle" on:click={toggleMenu} on:keypress={toggleMenu}>
      <span />
      <span />
      <span />
    </div>
    <ul class:show={showMenu}>
      <li><a href="#home" on:click={scrollToSection}>Home</a></li>
      <li><a href="#about" on:click={scrollToSection}>Chi sono</a></li>
      <li><a href="#services" on:click={scrollToSection}>Servizi</a></li>
      <li><a href="#structure" on:click={scrollToSection}>Struttura</a></li>
      <li><a href="#contacts" on:click={scrollToSection}>Contatti</a></li>
      
    </ul>
  </div>
</nav>

<style>
  nav {
    background-color: #006879;
    color: #fff;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 100;
    padding: 15px 0;
  }

  .nav-container {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
  }

  .logo img {
    height: 30px;
  }

  .menu-toggle {
    display: none;
    cursor: pointer;
  }

  .menu-toggle span {
    display: block;
    width: 25px;
    height: 3px;
    background-color: #fff;
    margin-bottom: 5px;
  }

  ul {
    display: flex;
    list-style-type: none;
    margin: 0;
    padding: 0;
  }

  ul li {
    margin-right: 25px;
  }

  ul li a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
  }

  ul.show {
    display: flex;
  }

  @media (max-width: 768px) {
    .menu-toggle {
      display: block;
    }

    .nav-container {
      justify-content: space-between;
    }

    ul {
      display: none;
      flex-direction: column;
      align-items: flex-start;
      padding: 20px;
      background-color: #006879;
      position: absolute;
      top: 100%;
      left: 0;
      width: 100%;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    ul.show {
      display: flex;
      height: 100vh;
    }
    ul li a {
      display: block;
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      font-size: 2.5rem;
      padding-left: 1.2rem;
      padding-bottom: 1rem;
    }
  }
</style>
