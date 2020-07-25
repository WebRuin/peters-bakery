<script>
  export let segment;
</script>

<style>
  nav {
    position: fixed;
    width: 450px;
    height: 100vh;
    background-color: var(--grey);
    font-weight: 300;
    border-right: 4px solid var(--white);
  }

  ul {
    height: 100%;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }

  li {
    display: block;
    float: left;
  }

  [aria-current] {
    position: relative;
    color: var(--gold);
    font-weight: bold;
    background-color: var(--darkTeal);
  }

  [aria-current]::before {
    position: absolute;
    display: block;
    content: "🍩";
    width: calc(100% - 1em);
    height: 2px;
    left: 11px;
    top: 15px;
  }

  a {
    display: flex;
    font-weight: bold;
    align-items: center;
    padding: 1rem 0 1rem 40px;
    color: var(--white);
    text-transform: uppercase;
    text-decoration: none;
    font-size: 1.25rem;
  }
</style>

<nav>
  <ul>
    <li>
      <a aria-current={segment === undefined ? 'page' : undefined} href=".">
        home
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'breads-pasties' ? 'page' : undefined}
        href="breads-pasties">
        breads & pasties
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'brownies-date_bars-cupcakes' ? 'page' : undefined}
        href="brownies-date_bars-cupcakes">
        brownies, date bars & cupcakes
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'doughnuts-danish' ? 'page' : undefined}
        href="doughnuts-danish">
        doughnuts & danish
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'coffee_cakes' ? 'page' : undefined}
        href="coffee_cakes">
        coffee cakes
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'cookies' ? 'page' : undefined}
        href="cookies">
        cookies
      </a>
    </li>
    <li>
      <a aria-current={segment === 'pies' ? 'page' : undefined} href="pies">
        pies
      </a>
    </li>
    <li>
      <a aria-current={segment === 'cakes' ? 'page' : undefined} href="cakes">
        cakes
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'seasonal-items' ? 'page' : undefined}
        href="seasonal-items">
        seasonal items
      </a>
    </li>
    <li>
      <a
        aria-current={segment === 'special-orders' ? 'page' : undefined}
        href="special-orders">
        special orders
      </a>
    </li>
  </ul>
</nav>
