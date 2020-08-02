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
  <title>Peter's Bakerey 🍩 Doughnuts & Danish</title>
</svelte:head>

<PageWrapper class="page-wrapper" title="Doughnuts & Danish">
  <Aside {images} />
  <div class="column">
    <H2>Doughnuts</H2>
    <ul>
      <li>
        Bars
        <ul>
          <li>Chocolate</li>
          <li>Double Chocolate</li>
          <li>Maple</li>
        </ul>
      </li>
      <li>Bizmark (fried cinnamon roll doughnut)</li>
      <li>Chocolate Cake</li>
      <li>Chocolate Twists</li>
      <li>Double Chocolate</li>
      <li>Cinnamon Cake</li>
      <li>Crumb Cake</li>
      <li>Glazed (Plain and Chocolate)</li>
      <li>Jelly</li>
      <li>Maple Glazed</li>
      <li>Plain Cake</li>
      <li>Powdered Cake</li>
      <li>Suger</li>
    </ul>
  </div>
  <div class="column">
    <H2>Danish</H2>
    <ul>
      <li>Apricot</li>
      <li>BearClaw</li>
      <li>Boysenberry</li>
      <li>Butterhorns (with or without almonds)</li>
      <li>Custard</li>
      <li>Figure 8 (glazed sweet dough Danish with or without almonds)</li>
      <li>Pineapple</li>
      <li>
        Pretzel (glazed sweet dough)
        <span class="superscript">* Weekends only</span>
      </li>
      <li />
    </ul>
  </div>
</PageWrapper>
