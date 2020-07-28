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
      srcset="doughnut-600.png 600w, doughnut-800.png 800w, doughnut.png 1200w,
      doughnut-1600.png 1600w"
      src="doughnut.png"
      alt="Sprinkled Doughnuts" />
    <Logo />
  </header>
{:else}
  <header class="subpage">
    <img
      srcset="doughnut-600.png 600w, doughnut-800.png 800w, doughnut.png 1200w,
      doughnut-1600.png 1600w"
      src="doughnut.png"
      alt="Sprinkled Doughnuts" />
    <SubpageLogo />
  </header>
{/if}
