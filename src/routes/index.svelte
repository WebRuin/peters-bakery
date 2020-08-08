<script>
  export let segment;
  import PageWrapper from "../components/PageWrapper.svelte";
</script>

<svelte:head>
  <title>Peter's Bakerey 🍩 {segment === undefined ? 'Home' : undefined}</title>
</svelte:head>

<PageWrapper title="Peter's Bakery">
  <figure>
    <img
      src="https://res.cloudinary.com/tihos/image/upload/w_1000,c_fill,ar_1:1,g_auto,r_max,/v1596476940/peters-bakery/cupcake-_storefront.jpg"
      alt="" />
  </figure>
</PageWrapper>
