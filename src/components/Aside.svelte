<script>
  import RotatingImages from "../components/RotatingImages.svelte";

  export let images;
</script>

<aside>
  <RotatingImages {images} speed={3000} />
</aside>
