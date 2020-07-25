<script>
  export let segment;
</script>

<style>
  .page-wrapper {
    width: calc(100% - 80px);
    min-height: 500px;
    margin: 40px auto;
    background-color: var(--white);
  }
</style>

<svelte:head>
  <title>Peter's Bakerey 🍩 {segment === undefined ? 'Home' : undefined}</title>
</svelte:head>

<section class="page-wrapper" />
