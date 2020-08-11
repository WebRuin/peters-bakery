<script>
  import H1 from "../components/H1.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

  export let segment;

  let width = 0;
  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/c_fill,e_auto_saturation,f_auto,h_500,q_auto,w_500/v1596346938/peters-bakery/walnut_nutbread.jpg"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/c_fill,e_auto_saturation,f_auto,h_500,q_auto,w_500/v1596346938/peters-bakery/filled_eclair.jpg"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/c_fill,e_auto_saturation,f_auto,h_500,q_auto,w_500/v1596346938/peters-bakery/spiced_bread.jpg"
    }
  ];
</script>

<style>
  figure {
    width: 90%;
    margin: 0 auto;
  }
</style>

<svelte:head>
  <title>Peter's Bakerey 🍩 {segment === undefined ? 'Home' : undefined}</title>
</svelte:head>

<PageWrapper>
  <Aside {images} />

  <H1>Peter's Bakery</H1>
  <figure>
    <img
      src="https://res.cloudinary.com/tihos/image/upload/w_1000,c_fill,ar_1:1,g_auto,r_max,/v1596476940/peters-bakery/cupcake-_storefront.jpg"
      alt="" />
  </figure>
</PageWrapper>
