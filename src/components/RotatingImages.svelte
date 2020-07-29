<script>
  import { onMount } from "svelte";
  export let images;
  export let speed;

  const pictures = images;
  let src = pictures[pictures.length - 1].src;
  let name = pictures[pictures.length - 1].name;
  let count = 0;

  console.log();

  const rotateImages = pictures => {
    src = pictures[count].src;
    name = pictures[count].name;
    count = count + 1;
    if (count >= pictures.length) count = 0;
  };

  setInterval(rotateImages, speed, pictures);
</script>

<style>
  figure {
    max-width: 80%;
    margin: 0 auto;
    overflow: hidden;
  }
  img {
    width: 200%;
  }
  img:hover {
    transform: scale(1.15);
  }
  @media (max-width: 1000px) {
    figure {
      margin-top: 0;
    }
    img {
      max-width: 100%;
      height: auto;
    }
  }
</style>

<figure>
  <img {src} alt="" `A picture of {name} ` />
  <figcaption>{name}</figcaption>
</figure>
