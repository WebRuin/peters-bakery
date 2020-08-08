<script>
  import Icon from "svelte-awesome";
  import { faTimesCircle } from "@fortawesome/free-regular-svg-icons";
  import { faBars } from "@fortawesome/free-solid-svg-icons";
  export let segment;

  let openOpen = false;

  function toggleNav() {
    openOpen = !openOpen;
  }
</script>

<style>
  nav {
    position: fixed;
    width: 450px;
    height: 100%;
    left: -450px;
    background: inherit;
    font-weight: 300;
    background-color: var(--darkTeal_95);
    border-right: 4px solid var(--hotPink);
    z-index: 9999999;
  }
  .open {
    left: 0;
  }
  .open > .navButton {
    left: 450px;
  }
  .navButton {
    position: fixed;
    left: 0;
    width: 40px;
    height: 40px;
    font-size: 2.5rem;
    background-color: var(--gold);
    color: var(--darkerTeal);
    z-index: 999;
  }
  ul {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }
  li {
    height: 100%;
  }
  [aria-current] {
    position: relative;
    color: var(--white);
    font-weight: bold;
    background-color: var(--hotPink);
  }
  [aria-current]::before {
    position: absolute;
    display: block;
    content: "🧁";
    width: calc(100% - 1em);
    height: 28px;
    left: -190px;
    top: 50%;
    margin-top: -14px;
  }
  button.link {
    width: 100%;
    height: inherit;
    padding: 0;
    border: none;
    outline: none;
    user-select: none;
    background-color: transparent;
  }
  a {
    width: 100%;
    height: inherit;
    display: flex;
    font-weight: bold;
    align-items: center;
    padding: 1rem 0 1rem 40px;
    color: var(--white);
    text-transform: uppercase;
    text-decoration: none;
    font-size: 1.25rem;
  }

  @media (max-width: 1000px) {
    nav {
      position: absolute;
    }
    ul {
      height: auto;
    }
    .navButton {
      position: absolute;
      top: 0;
      left: 450px;
      max-width: 30px;
      height: 30px;
      z-index: 99;
    }
    nav {
      width: 450px;
    }
    a {
      font-size: 1rem;
    }
  }
</style>

<nav class={openOpen ? 'open' : ''}>

  <button class="navButton" on:click={toggleNav}>
    {#if openOpen == true}
      <Icon scale="3" data={faTimesCircle} flip="horizontal" />
    {:else}
      <Icon scale="2" data={faBars} flip="horizontal" />
    {/if}
  </button>
  <ul>
    <li>
      <button on:click={toggleNav} class="link">
        <a aria-current={segment === undefined ? 'page' : undefined} href=".">
          home
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'breads-pastries' ? 'page' : undefined}
          href="breads-pastries">
          breads & pastries
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'brownies-date_bars-cupcakes' ? 'page' : undefined}
          href="brownies-date_bars-cupcakes">
          brownies, date bars & cupcakes
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'doughnuts-danish' ? 'page' : undefined}
          href="doughnuts-danish">
          doughnuts & danish
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'coffee-cakes_cookies' ? 'page' : undefined}
          href="coffee-cakes_cookies">
          coffee cakes & cookies
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a aria-current={segment === 'pies' ? 'page' : undefined} href="pies">
          pies
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a aria-current={segment === 'cakes' ? 'page' : undefined} href="cakes">
          cakes
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'seasonal-items' ? 'page' : undefined}
          href="seasonal-items">
          seasonal items
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'special-orders' ? 'page' : undefined}
          href="special-orders">
          special orders
        </a>
      </button>
    </li>
  </ul>
</nav>
