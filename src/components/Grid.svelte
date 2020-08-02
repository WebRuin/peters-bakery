<script>
  export let wrap;
</script>

<style>
  .grid {
    display: flex;
    justify-content: space-between;
    gap: 3rem;
    min-height: 500px;
    padding: 1rem 250px 1em 500px;
  }
  @media (max-width: 1000px) {
    .grid {
      padding: 0;
      grid-gap: 0;
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="grid {wrap ? 'wrap' : ''}">
  <slot />
</div>
