<style>
  h1 {
    text-align: center;
    color: var(--hotPink);
    font-size: 3.75rem;
    font-family: "Pacifico", cursive;
  }
  span {
    background-color: var(--teal_75);
    padding: 1rem;
    margin: 1rem;
  }
  @media (max-width: 1000px) {
    h1 {
      margin-top: -2rem;
      font-size: 1.75rem;
    }
    span {
      padding: 0.5rem;
      margin: 0.5rem;
    }
  }
</style>

<h1>
  <span>
    <slot />
  </span>
</h1>
