<style>
  .grid {
    display: flex;
    justify-content: space-between;
    gap: 3rem;
    min-height: 500px;
    padding: 1rem 100px 1em 650px;
  }
  @media (max-width: 1000px) {
    .grid {
      padding: 0;
      gap: 0;
      flex-wrap: wrap;
    }
  }
</style>

<section class="grid">
  <slot />
</section>
