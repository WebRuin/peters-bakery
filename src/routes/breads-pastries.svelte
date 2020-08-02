<script>
  import H2 from "../components/H2.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

  const images = [
    {
      src:
        "https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595917680/peters-bakery/bread.png",
      name: "Cinnamon Nut Bread"
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
  <title>Peter's Bakerey 🍩 Breads & Pastries</title>
</svelte:head>

<PageWrapper title="Breads & Pastries">
  <Aside {images} />
  <div>
    <H2>Breads</H2>
    <ul>
      <li>Almond Poppy Seed Loaf</li>
      <li>Banana Nut Bread</li>
      <li>Blueberry Loaf</li>
      <li>Cinnamon Nut Bread</li>
      <li>Dinner Rolls</li>
      <li>English Tea Cake (Maple Flavored)</li>
      <li>Lemon Loaf</li>
      <li>Portugese Sweet Bread</li>
      <li>Potato Bread (Sliced)</li>
      <li>White Bread (Sliced)</li>
    </ul>
  </div>
  <div>
    <H2>Pastries</H2>
    <ul>
      <li>
        Muffins
        <ul>
          <li>Bannana Nut</li>
          <li>Blueberry</li>
          <li>Bran</li>
          <li>Cholcolate Chip</li>
          <li>Orange</li>
        </ul>
      </li>
      <li>
        Rolls
        <ul>
          <li>Nut</li>
          <li>Orange</li>
          <li>Raspberry</li>
        </ul>
      </li>
      <li>Apple Squares</li>
      <li>Apple Turnovers</li>
      <li>Cinnamon Squares</li>
      <li>Croissants</li>
    </ul>
    <H2>Whipped Cream Pastries</H2>
    <ul>
      <li>Apple Turn Over</li>
      <li>Cream Horns</li>
      <li>Cream Puffs</li>
      <li>Éclairs (Whipped Cream or Custard)</li>
      <li>Tarts</li>
    </ul>
  </div>
</PageWrapper>
