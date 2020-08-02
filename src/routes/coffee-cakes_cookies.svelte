<script>
  import H2 from "../components/H2.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957503/peters-bakery/Screenshot_2020-07-28_menu_pdf_5.png",
      name: "Plain Coffee Cake with custard filling"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957506/peters-bakery/Screenshot_2020-07-28_menu_pdf_6.png",
      name: "Pfefferneuse"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957503/peters-bakery/Screenshot_2020-07-28_menu_pdf_7.png",
      name: "Holidays Cutouts (St. Patrick's)"
    }
  ];
</script>

<svelte:head>
  <title>Peter's Bakerey 🍩 Coffee Cakes & Cookies</title>
</svelte:head>

<PageWrapper title="Coffee Cakes">
  <Aside {images} />
  <div class="column">
    <H2>Coffee Cake</H2>
    <ul>
      <li>Apple</li>
      <li>Apricot</li>
      <li>Bear Claw</li>
      <li>Berry</li>
      <li>Custard</li>
      <li>German</li>
      <li>Pineapple</li>
      <li>Plain (with or without almonds)</li>
    </ul>
  </div>
  <div class="column">
    <H2>Cookies</H2>
    <ul>
      <li>Chocolate Chip and Nuts</li>
      <li>Chocolate Drops</li>
      <li>Chocolate/Vanilla Swirl</li>
      <li>Cinnamon with Nuts</li>
      <li>English Rock</li>
      <li>Fruit Bar (Maple bar with mixed nuts)</li>
      <li>Mexican Wedding Cookies</li>
      <li>Oatmeal Raisin</li>
      <li>Shortbread</li>
      <li>Sugar</li>
    </ul>
  </div>
</PageWrapper>
