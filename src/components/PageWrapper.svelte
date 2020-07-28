<script>
  import H1 from "../components/H1.svelte";
  import Grid from "../components/Grid.svelte";

  export let title;
  export let image;
  export let altText;
</script>

<style>
  .page-wrapper {
    width: calc(100% - 80px);
    min-height: 500px;
    margin: 40px auto;
    background-color: var(--white);
    font-size: 2rem;
  }
  figure {
    margin-top: 6rem;
    width: 100%;
    overflow: hidden;
  }
  img {
    width: inherit;
  }
  @media (max-width: 1000px) {
    .page-wrapper {
      width: auto;
      margin: 30px 10px 10px 10px;
      margin-bottom: -1rem;
      padding: 1rem;
      padding-top: 2rem;
      font-size: 1rem;
    }
    figure {
      margin-top: 0;
    }
    img {
      max-width: 100%;
      height: auto;
    }
  }
</style>

<article class="page-wrapper">
  <H1>{title}</H1>
  <Grid>
    <figure>
      <img src={image} alt={altText} />
    </figure>
    <slot />
  </Grid>
</article>
