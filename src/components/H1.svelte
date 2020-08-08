<style>
  h1 {
    position: relative;
    z-index: 99999;
    text-align: center;
    color: var(--teal);
    margin-left: 250px;
    font-family: "Pacifico", cursive;
    text-shadow: 3px 3px 0 var(--darkerTeal), 6px 6px 0 var(--darkPink);
  }
  @media (max-width: 1000px) {
    h1 {
      margin-top: -2rem;
      margin-left: 250px;
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
