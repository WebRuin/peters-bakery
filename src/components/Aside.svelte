<script>
  import RotatingImages from "../components/RotatingImages.svelte";

  export let images;
</script>

<style>
  aside {
    width: 90%;
    margin: 0 auto;
  }
  @media (min-width: 1000px) {
    aside {
      position: absolute;
      top: 0;
      left: 40px;
      width: 453px;
      height: 100%;
      padding-top: 424px;
      padding-left: 43px;
      background-color: var(--hotPink_75);
      border-right: 3px solid var(--darkerTeal);
    }
  }
</style>

<aside>
  <RotatingImages {images} speed={3000} />
</aside>
