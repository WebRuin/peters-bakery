<script>
  import H2 from "../components/H2.svelte";
  import H3 from "../components/H3.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957507/peters-bakery/Screenshot_2020-07-28_menu_pdf_10.png",
      name: "Decorated Burnt Almond"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957507/peters-bakery/Screenshot_2020-07-28_menu_pdf_11.png",
      name: "Carrot Cake"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957508/peters-bakery/Screenshot_2020-07-28_menu_pdf_12.png",
      name: "Baby Shower Cake"
    }
  ];
</script>

<svelte:head>
  <title>Peter's Bakerey 🍩 Cakes</title>
</svelte:head>

<PageWrapper title="Cakes" wrap={true}>
  <Aside {images} />
  <div class="column">
    <H2>Cakes</H2>
    <H3>Available in store every day while supples last</H3>
    <ul>
      <li>All Chocolate</li>
      <li>Angel Food</li>
      <li>Berry Boston</li>
      <li>Burnt Almond</li>
      <li>Carrot Cake</li>
      <li>Checkerboard</li>
      <li>German Chocolate</li>
      <li>Lemon Crunch</li>
      <li>Orange Chiffron</li>
      <li>Red Velvet</li>
      <li>Shirley Special</li>
    </ul>
  </div>
  <div class="column">
    <H2>White Cakes</H2>
    <ul>
      <li>Chocolate Icing</li>
      <li>Buttercream</li>
      <li>Buttercream & Walnuts</li>
      <li>Buttercream & Coconut</li>
      <li>Whip Cream & Pineapple</li>
      <li>Whip Cream & Bananas</li>
    </ul>
  </div>
  <div class="column">
    <H2>Seasonal Cakes</H2>
    <ul>
      <li>White Cake w/ Whipped Cream & StawBerries</li>
      <li>Whip Cream & Bananas</li>
      <li>Buttercream & Chololate Shavings</li>
      <li>Whip Cream & Bananas</li>
    </ul>
  </div>
</PageWrapper>
