<script>
  import PageWrapper from "../components/PageWrapper.svelte";
  import H1 from "../components/H1.svelte";

  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595917680/peters-bakery/bread.png",
      name: "Cinnamon"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957962/peters-bakery/Screenshot_2020-07-28_menu_pdf_18.png",
      name: "Strawberry Ring"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957500/peters-bakery/Screenshot_2020-07-28_menu_pdf.png",
      name: "Éclairs"
    }
  ];
</script>

<svelte:head>
  <title>Peter's Bakerey 🍩 Brownies, Date Bars & Cupcakes</title>
</svelte:head>

<PageWrapper
  title="Brownies, Date Bars & Cupcakes"
  {images}
  altText="A picture of bread">
  hi
</PageWrapper>
