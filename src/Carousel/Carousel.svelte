<script>
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  let img4 = "assets/PAL1.jpg";
  let img1 = "assets/PAL2.jpg";
  let img6 = "assets/PAL3.jpg";
  let img5 = "assets/PAL4.jpg";
  let img3 = "assets/PAL5.jpg";
  let img2 = "assets/PAL6.jpg";
</script>

<Splide aria-label="My Favorite Images"  options={ {
    rewind: true,
    width : 800,
    gap   : '1rem',
  } }>
  <SplideSlide>
    <div class="img-div">
        <img src={img1} alt="Immagine della palestra" />
    </div>
  </SplideSlide>
  <SplideSlide>
    <div class="img-div">
        <img src={img2} alt="Immagine della palestra" />
    </div>
  </SplideSlide>
  <SplideSlide>
    <div class="img-div">
        <img src={img3} alt="Immagine della palestra"/>
    </div>
  </SplideSlide>
  <SplideSlide>
    <div class="img-div">
        <img src={img4} alt="Immagine della palestra" />
    </div>
  </SplideSlide>
  <SplideSlide>
    <div class="img-div">
        <img src={img5} alt="Immagine della palestra" />
    </div>
  </SplideSlide>
  <SplideSlide>
    <div class="img-div">
        <img src={img6} alt="Immagine della palestra"/>
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