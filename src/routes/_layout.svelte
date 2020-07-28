<script>
  import Nav from "../components/Nav.svelte";
  import Header from "../components/Header.svelte";

  export let segment;
</script>

<style>
  main {
    position: relative;
  }
</style>

<Nav {segment} />

<main>
  <Header {segment} />
  <slot />
</main>
