<script>
  import H1 from "../components/H1.svelte";
</script>

<style>
  .page-wrapper {
    width: calc(100% - 80px);
    min-height: 500px;
    margin: 40px auto;
    background-color: var(--white);
    font-size: 2rem;
  }

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

  .grid {
    padding: 4rem;
    display: grid;
    grid-gap: 4rem;
    grid-template-columns: repeat(3, 1fr);
  }

  figure {
    margin-top: 6rem;
    width: 100%;
    overflow: hidden;
  }

  img {
    width: 100%;
  }
  img:hover {
    transform: scale(1.25);
  }
  ul {
    width: 600px;
  }

  ul ul {
    margin: 0.25rem 1rem;
  }

  ul ul li {
    list-style: disc;
    margin-left: 2.5rem;
  }
  li {
    list-style: none;
    color: var(--darkTeal);
  }
</style>

<svelte:head>
  <title>Peter's Bakerey 🍩 Breads & Pastries</title>
</svelte:head>

<section class="page-wrapper">
  <H1>Breads & Pastries</H1>
  <section class="grid">
    <figure>
      <img src="./bread.png" alt="A picture of bread" />
    </figure>
    <ul>
      <h2>Breads</h2>
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
    <ul>
      <h2>Pasties</h2>
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
  </section>
</section>
