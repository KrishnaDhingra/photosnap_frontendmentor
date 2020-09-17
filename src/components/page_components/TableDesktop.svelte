<script>
  const features = [
    {name: 'Unlimited Story Posting', basic: true, pro: true, business: true },
    {name: 'Unlimited Photo Upload', basic: true, pro: true, business: true },
    {name: 'Embedding Custom Content', basic: false, pro: true, business: true },
    {name: 'Customize Metadata', basic: false, pro: true, business: true },
    {name: 'Advanced Metrics', basic: false, pro: false, business: true },
    {name: 'Photo Downloads', basic: false, pro: false, business: true },
    {name: 'Search Engine Indexing', basic: false, pro: false, business: true },
    {name: 'Custom Analytics', basic: false, pro: false, business: true }
  ];
</script>

<div class="container">
  <h2 class="t-heading t-black table-heading">Compare</h2>

  <div class="table">
  <div class="table-row table-row--heading">
    <span class="table__heading t-pickplan t-black">The Features</span>
    <span class="table__heading t-pickplan t-black">Basic</span>
    <span class="table__heading t-pickplan t-black">Pro</span>
    <span class="table__heading t-pickplan t-black">Business</span>
  </div>
  {#each features as feature}
    <div class="table-row table-row--body">
      <span class="table__body t-pickplan t-black">{feature.name}</span>
      <span class="plan__check{feature.basic ? ' checked': ''}"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="15"><path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1"/></svg></span>
      <span class="plan__check{feature.pro ? ' checked': ''}"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="15"><path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1"/></svg></span>
      <span class="plan__check{feature.business ? ' checked': ''}"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="15"><path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1"/></svg></span>
    </div>
  {/each}
  </div>
</div>

<style>
  .container {
    margin: 0 auto;
    max-width: 73.1rem;
  }
  .table-heading {
    text-align: center;
    margin-bottom: 6.4rem;
  }
  @media (min-width: 1200px) {
    .table-heading {
      margin-bottom: 5.6rem;
    }
  }

  .plan__check {
    opacity: 0;
  }
  .plan__check.checked {
    opacity: 1;
  }

  .table-row {
    display: grid;
    grid-template-columns: 1fr repeat(3, 14rem);
  }

  .table__heading:not(:first-of-type) {
    justify-self: center;
  }

  .table__heading:first-of-type {
    padding-left: 2.4rem;
  }

  .plan__check {
    justify-self: center;
  }

  .table-row--heading {
    padding-bottom: 2.3rem;
    border-bottom: 1px solid var(--color-black);
  }
  .table-row--body {
    padding: 2.3rem 0;
    border-bottom: 1px solid var(--color-gray);
  }

  .table__body {
    padding-left: 2.4rem;
  }
</style>
