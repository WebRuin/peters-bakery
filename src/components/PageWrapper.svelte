<script>
  import Grid from "../components/Grid.svelte";
</script>

<style>
  .page-wrapper {
    width: calc(100% - 80px);
    min-height: 500px;
    padding-top: 1rem;
    margin: 2px auto 1rem auto;
    background-color: var(--white);
    /* font-size: 2rem; */
  }
  @media (max-width: 1000px) {
    .page-wrapper {
      width: auto;
      margin: 30px 10px 10px 10px;
      margin-bottom: -1rem;
      padding: 3rem 1rem 1rem 1rem;
      /* font-size: 1rem; */
    }
  }
</style>

<article class="page-wrapper">
  <Grid>
    <slot />
  </Grid>
</article>
