<script>
  import Nav from "../components/Nav.svelte";
  import Header from "../components/Header.svelte";

  export let segment;
</script>

<style>
  .wrapper {
    position: relative;
  }
  main {
    position: relative;
    background-color: var(--darkGrey);
    box-sizing: border-box;
    width: calc(100% - 450px);
    margin-left: auto;
  }
</style>

<div class="wrapper">
  <Nav {segment} />

  <main>
    <Header {segment} />
    <slot />
  </main>
</div>
