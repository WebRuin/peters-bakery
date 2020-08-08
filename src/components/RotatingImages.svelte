<script>
  import { onMount } from "svelte";

  // Props
  export let images;
  export let speed;

  const pictures = images;

  const cloud_name = "tihos";
  let src = images[images.length - 1].src;
  let count = 0;

  function rotateImages(images) {
    src = images[count].src;
    count = count + 1;
    if (count >= images.length) count = 0;
  }

  setInterval(rotateImages, speed, images);
</script>

<style>
  figure {
    overflow: hidden;
    margin-left: -43px;
  }

  img {
    width: 200%;
  }
  img:hover {
    transform: scale(1.05);
  }
  @media (max-width: 1000px) {
    figure {
      margin-top: 0;
      margin: 0 auto;
    }
    img {
      max-width: 100%;
      height: auto;
    }
  }
</style>

<figure>
  <img {src} alt="" />
</figure>
