<script>
  import Fa from "svelte-fa";
  import {
    faPersonWalking,
    faAppleWhole,
    faBuildingCircleCheck,
    faDumbbell
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

<section id="structure">
  <h5>I miei servizi</h5>
  <h1>Lorem ipsum dolor sit amet</h1>
  <ul>
    <li class="list-item">
      <Fa icon={faAppleWhole} />
      <p class="item-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </p>
    </li>
    <li class="list-item">
      <Fa icon={faPersonWalking} />
      <p class="item-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </p>
    </li>
  </ul>

  <Carousel />

  <h5>La struttura</h5>
  <h1>Lorem ipsum dolor sit amet</h1>
  <ul>
    <li class="list-item">
      <Fa icon={faDumbbell} />
      <p class="item-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </p>
    </li>
    <li class="list-item">
      <Fa icon={faBuildingCircleCheck} />
      <p class="item-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </p>
    </li>
  </ul>

  <Youtube id="K4TOrB7at0Y" />

</section>

<style>
  #structure {
    margin-left: 1rem;
    margin-right: 1rem;
  }

  ul {
    padding-inline-start: 0px;
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
