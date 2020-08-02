<script>
  import H2 from "../components/H2.svelte";
  import H3 from "../components/H3.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957505/peters-bakery/Screenshot_2020-07-28_menu_pdf_8.png",
      name: "Pumpkin Pie"
    },
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595957507/peters-bakery/Screenshot_2020-07-28_menu_pdf_9.png",
      name: "Chocolate Cream Pie"
    }
  ];
</script>

<svelte:head>
  <title>Peter's Bakerey 🍩 Pies</title>
</svelte:head>

<PageWrapper title="Pies">
  <Aside {images} />
  <div class="column">
    <H2>Fruit Pies</H2>
    <H3>Available Everyday</H3>
    <ul>
      <li>Apple</li>
      <li>Apricot</li>
      <li>Berry</li>
      <li>Cherry</li>
      <li>Dutch Apple</li>
      <li>Lemon</li>
      <li>Peach</li>
      <li>Pumpkin</li>
    </ul>
  </div>
  <div class="column">
    <H2>Whipped Cream Pie</H2>
    <ul>
      <li>Bannana Cream (Friday & Saturday)</li>
      <li>Apricot (Special order)</li>
      <li>Coconut (Friday & Sarurday)</li>
      <li>Chocolate (Every Day)</li>
      <li>Lemon Cream (Every Day)</li>
    </ul>
  </div>
</PageWrapper>
