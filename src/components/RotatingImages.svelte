<script>
  import { onMount } from "svelte";

  // Props
  export let images;
  export let speed;

  const pictures = images;

  let src = images[images.length - 1].src;
  let name = images[images.length - 1].name;
  let count = 0;

  console.log();

  function rotateImages(images) {
    src = images[count].src;
    name = images[count].name;
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
  figcaption {
    width: 100%;
    display: grid;
    font-size: 2.5rem;
    justify-content: center;
    color: var(--white);
    margin-top: 0.5rem;
    padding-bottom: 0.5rem;
    text-shadow: 2px 2px 0 var(--darkTeal), 4px 4px 0 var(--gold);
    font-family: "Pacifico", cursive;
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
    }
    img {
      max-width: 100%;
      height: auto;
    }
  }
</style>

<figure>
  <img {src} alt="A picture of {name}" />
  <figcaption>{name}</figcaption>
</figure>
