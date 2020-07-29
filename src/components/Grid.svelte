<style>
  .grid {
    padding: 1rem 3rem;
    display: grid;
    grid-gap: 3rem;
    grid-template-columns: repeat(3, 1fr);
  }
  @media (max-width: 1000px) {
    .grid {
      padding: 0;
      grid-gap: 0;
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="grid">
  <slot />
</div>
