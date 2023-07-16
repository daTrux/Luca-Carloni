<script>
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  let img1 = "assets/PAL1.jpg";
  let img2 = "assets/PAL2.jpg";
</script>

<Splide aria-label="My Favorite Images"  options={ {
    rewind: true,
    width : 800,
    gap   : '1rem',
  } }>
  <SplideSlide>
    <div class="img-div">
        <img src={img1}>
    </div>
  </SplideSlide>
  <SplideSlide>
    <div class="img-div">
        <img src={img2}>
    </div>
  </SplideSlide>
</Splide>
<style>
    .img-div {
        max-width: 100%;
        height: auto;
    }
    img {
        max-width: 100%;
    }
    </style>