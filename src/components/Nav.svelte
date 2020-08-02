<script>
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
  .navButton {
    position: absolute;
    left: 450px;
    width: 40px;
    height: 40px;
    font-size: 2.5rem;
    background-color: var(--gold);
    color: var(--hotPink);
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
      width: 2rem;
      height: 2rem;
    }
    .navButton svg {
      width: 1rem !important;
      width: auto;
      background-size: cover;
    }
    nav {
      width: 100vw;
    }
    a {
      font-size: 1rem;
    }
  }
</style>

<nav class={openOpen ? 'open' : ''}>

  <button class="navButton" on:click={toggleNav}>
    {#if openOpen == true}
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="icon icon-tabler icon-tabler-circle-x"
        width="44"
        height="44"
        viewBox="0 0 24 24"
        stroke-width="2.5"
        stroke="currentColor"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round">
        <path stroke="none" d="M0 0h24v24H0z" />
        <circle cx="12" cy="12" r="9" />
        <path d="M10 10l4 4m0 -4l-4 4" />
      </svg>
    {:else}
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="icon icon-tabler icon-tabler-menu"
        width="44"
        height="44"
        viewBox="0 0 24 24"
        stroke-width="2.5"
        stroke="currentColor"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round">
        <path stroke="none" d="M0 0h24v24H0z" />
        <line x1="4" y1="8" x2="20" y2="8" />
        <line x1="4" y1="16" x2="20" y2="16" />
      </svg>
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
