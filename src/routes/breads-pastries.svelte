<script>
  import PageWrapper from "../components/PageWrapper.svelte";
</script>

<style>
  h2 {
    position: relative;
    color: var(--peach);
    margin-bottom: 10px;
  }
  h2::after {
    position: absolute;
    left: 0;
    bottom: -5px;
    content: "";
    height: 4px;
    width: 100%;
    background-color: var(--grey);
  }
</style>

<svelte:head>
  <title>Peter's Bakerey 🍩 Breads & Pastries</title>
</svelte:head>

<PageWrapper
  title="Breads & Pastries"
  image="./bread.png"
  altText="A picture of bread">
  <div>
    <h2>Breads</h2>
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
    <h2>Pasties</h2>
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
  </div>
</PageWrapper>
