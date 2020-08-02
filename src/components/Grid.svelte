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
      gap: 0;
      flex-wrap: wrap;
    }
  }
</style>

<div class="grid {wrap ? 'wrap' : ''}">
  <slot />
</div>
