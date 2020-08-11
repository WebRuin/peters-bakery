<style>
  h1 {
    text-align: center;
    color: var(--teal);
    /* margin-bottom: 2rem; */
    font-family: "Pacifico", cursive;
    text-shadow: 3px 3px 0 var(--darkerTeal), 6px 6px 0 var(--darkPink);
    transform: rotate(270deg);
    height: 100%;
    width: 100%;
    margin: 0 -65% 0 -5%;
  }
  @media (max-width: 1000px) {
    h1 {
      margin-top: -2rem;
    }
  }
</style>

<h1>
  <slot />
</h1>
