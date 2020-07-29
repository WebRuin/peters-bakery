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
    z-index: 999;
  }
  .open {
    left: 0;
  }
  .navButton {
    position: absolute;
    left: 450px;
    width: 50px;
    height: 50px;
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
        aria-hidden="true"
        focusable="false"
        data-prefix="far"
        data-icon="times-circle"
        class="svg-inline--fa fa-times-circle fa-w-16"
        role="img"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 512 512">
        <path
          fill="currentColor"
          d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256
          8zm0 448c-110.5 0-200-89.5-200-200S145.5 56 256 56s200 89.5 200
          200-89.5 200-200 200zm101.8-262.2L295.6 256l62.2 62.2c4.7 4.7 4.7 12.3
          0 17l-22.6 22.6c-4.7 4.7-12.3 4.7-17 0L256 295.6l-62.2 62.2c-4.7
          4.7-12.3 4.7-17 0l-22.6-22.6c-4.7-4.7-4.7-12.3
          0-17l62.2-62.2-62.2-62.2c-4.7-4.7-4.7-12.3 0-17l22.6-22.6c4.7-4.7
          12.3-4.7 17 0l62.2 62.2 62.2-62.2c4.7-4.7 12.3-4.7 17 0l22.6 22.6c4.7
          4.7 4.7 12.3 0 17z" />
      </svg>
    {:else}
      <svg
        aria-hidden="true"
        focusable="false"
        data-prefix="fas"
        data-icon="bars"
        class="svg-inline--fa fa-bars fa-w-14"
        role="img"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 448 512">
        <path
          fill="currentColor"
          d="M16 132h416c8.837 0 16-7.163
          16-16V76c0-8.837-7.163-16-16-16H16C7.163 60 0 67.163 0 76v40c0 8.837
          7.163 16 16 16zm0 160h416c8.837 0 16-7.163
          16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837
          7.163 16 16 16zm0 160h416c8.837 0 16-7.163
          16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837
          7.163 16 16 16z" />
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
          aria-current={segment === 'coffee_cakes' ? 'page' : undefined}
          href="coffee_cakes">
          coffee cakes
        </a>
      </button>
    </li>
    <li>
      <button on:click={toggleNav} class="link">
        <a
          aria-current={segment === 'cookies' ? 'page' : undefined}
          href="cookies">
          cookies
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
