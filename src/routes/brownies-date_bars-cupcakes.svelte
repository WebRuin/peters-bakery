<script>
  import H2 from "../components/H2.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957501/peters-bakery/Screenshot_2020-07-28_menu_pdf_1.png",
      name: "Cupcakes"
    }
  ];
</script>

<svelte:head>
  <title>Peter's Bakerey 🍩 Brownies, Date Bars & Cupcakes</title>
</svelte:head>

<PageWrapper title="Brownies, Date Bars & Cupcakes" wrap={true}>
  <Aside {images} />
  <div class="column">
    <H2>Brownies</H2>
    <ul>
      <li>Chocolate brownie with walnuts and chocolate fugge icing</li>
    </ul>
  </div>
  <div class="column">
    <H2>Date Bars</H2>
    <ul>
      <li>Date mix with a buttery crumb topping</li>
    </ul>
  </div>
  <div class="column">
    <H2>Cupcakes</H2>
    <ul>
      <li>
        White or Chocolate cake iceing options
        <ul>
          <li>Buttercream</li>
          <li>Whipped Cream</li>
          <li>Shirley</li>
          <li>Lemon</li>
          <li>Chocolate</li>
          <li>Coconut</li>
          <li>Burnt Almond</li>
        </ul>
      </li>
    </ul>
  </div>
</PageWrapper>
