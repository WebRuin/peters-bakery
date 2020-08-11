<style>
  .grid {
    display: grid;
    grid-template-columns: 450px auto;
    gap: 1rem;
    min-height: 500px;
    /* padding: 1rem 100px 1em 650px; */
  }
  .flex {
    display: flex;
    justify-content: space-evenly;
  }
  @media (max-width: 1000px) {
    .grid {
      grid-template-columns: auto;
      grid-template-rows: auto 1fr;
      padding: 0;
      gap: 0;
    }
    .flex {
      flex-wrap: wrap;
    }
  }
</style>

<section class="grid">
  <div />
  <div class="flex">
    <slot title />
  </div>
</section>
