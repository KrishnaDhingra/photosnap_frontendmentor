<script>
  import TableMobile from './TableMobile.svelte';
  import TableDesktop from './TableDesktop.svelte';
</script>

<section class="compare">
  <div class="compare__mobile">
    <TableMobile/>
  </div>
  <div class="compare__desktop">
    <TableDesktop/>
  </div>
</section>

<style>
  .compare__mobile {
    padding-left: 2.9rem;
    padding-right: 2.8rem;
    padding-bottom: 6.4rem;
  }
  @media (min-width: 768px) {
    .compare__mobile {
      display: none;
    }
  }

  .compare__desktop {
    display: none;
  }
  @media (min-width: 768px) {
    .compare__desktop {
      display: block;
    }
  }

</style>