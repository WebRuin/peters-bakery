<style>
  h1 {
    position: relative;
    z-index: 99999;
    text-align: center;
    color: var(--hotPink);
    font-family: "Pacifico", cursive;
    text-shadow: 3px 3px 0 var(--teal), 6px 6px 0 var(--teal);
  }
  @media (max-width: 1000px) {
    h1 {
      margin-top: -2rem;
    }
    span {
      padding: 0.5rem;
      margin: 0.5rem;
    }
  }
</style>

<h1>
  <slot />
</h1>
