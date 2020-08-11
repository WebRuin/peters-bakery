<style>
  h2 {
    margin-top: -1rem;
    color: var(--gold);
    grid-column-start: 2;
    grid-column-end: 3;
    font-family: "Pacifico", cursive;
    text-transform: capitalize;
    text-shadow: 3px 3px 0 var(--hotPink), 6px 6px 0 var(--teal);
  }
  @media (max-width: 1000px) {
    h2 {
      margin-top: 0;
    }
  }
</style>

<h2>
  <slot />
</h2>
