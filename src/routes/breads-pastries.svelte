<script>
  import H1 from "../components/H1.svelte";
  import H2 from "../components/H2.svelte";
  import PageWrapper from "../components/PageWrapper.svelte";
  import Aside from "../components/Aside.svelte";

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

<svelte:head>
  <title>Peter's Bakerey 🍩 Breads & Pastries</title>
</svelte:head>

<PageWrapper title="">
  <Aside {images} />

  <H1>Breads & Pastries</H1>
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
