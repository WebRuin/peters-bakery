<script>
  import { onMount } from "svelte";
  import H1 from "../components/H1.svelte";
  import Grid from "../components/Grid.svelte";

  export let title;
  export let wrap;
</script>

<style>
  .page-wrapper {
    width: calc(100% - 80px);
    min-height: 500px;
    margin: 40px auto 1rem auto;
    background-color: var(--white);
    /* font-size: 2rem; */
  }
  @media (max-width: 1000px) {
    .page-wrapper {
      width: auto;
      margin: 30px 10px 10px 10px;
      margin-bottom: -1rem;
      padding: 1rem;
      padding-top: 2rem;
      /* font-size: 1rem; */
    }
  }
</style>

<article class="page-wrapper">
  <H1>{title}</H1>
  <Grid {wrap}>
    <slot />
  </Grid>
</article>
