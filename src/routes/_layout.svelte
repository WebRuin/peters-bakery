<script>
  import Nav from "../components/Nav.svelte";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";

  // export let segment;
</script>

<style>
  main {
    position: relative;
  }
</style>

<Nav />

<main>
  <Header />
  <slot />
</main>

<Footer />
