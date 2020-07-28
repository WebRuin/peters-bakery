<script>
  import Logo from "../components/Logo.svelte";
  import SubpageLogo from "../components/SubpageLogo.svelte";

  export let segment;
</script>

<style>
  header {
    position: relative;
    height: 475px;
    overflow: hidden;
    border-bottom: 30px solid var(--gold);
  }
  header.subpage {
    height: 237.5px;
    border-bottom: 15px solid var(--gold);
  }
  img {
    width: 100%;
  }
  @media (max-width: 1000px) {
    header {
      border-bottom: 8px solid var(--gold) !important;
    }

    img {
      height: 100%;
    }
  }
</style>

{#if segment === undefined}
  <header>
    <img
      src="https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595917525/peters-bakery/doughnut-1600.png"
      alt="Sprinkled Doughnuts" />
    <Logo />
  </header>
{:else}
  <header class="subpage">
    <img
      src="https://res.cloudinary.com/tihos/image/upload/f_auto,q_auto/v1595917525/peters-bakery/doughnut-1600.png"
      alt="Sprinkled Doughnuts" />
    <SubpageLogo />
  </header>
{/if}
