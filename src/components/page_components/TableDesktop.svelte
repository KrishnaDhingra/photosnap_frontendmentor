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
  {#each features as feature}
    <div class="table-row">
      <div class="plan-head t-black">{feature.name}</div>
      <div class="plan-body">
        <div class="plan">
          <span class="plan__name">Basic</span>
          <span class="plan__check{feature.basic ? ' checked': ''}"><span class="feature-check checked"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="15"><path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1"/></svg></span>
        </div>
        <div class="plan">
          <span class="plan__name">Pro</span>
          <span class="plan__check{feature.pro ? ' checked': ''}"><span class="feature-check checked"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="15"><path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1"/></svg></span>
        </div>
        <div class="plan">
          <span class="plan__name">Business</span>
          <span class="plan__check{feature.business ? ' checked': ''}"><span class="feature-check checked"><svg xmlns="http://www.w3.org/2000/svg" width="18" height="15"><path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1"/></svg></span>
        </div>
      </div>
      <div class="divider-row"></div>
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
  }
  
  .divider-row {
    width: 100%;
    height: .1rem;
    background-color: var(--color-gray);
    margin-bottom: 1px solid var(--color-gray);
  }
  .plan-head {
    width: 100%;
    font-size: 1.2rem;
    line-height: 1.6rem;
    margin-bottom: 1.6rem;
    letter-spacing: .2rem;
    text-transform: uppercase;
    font-weight: var(--weight-bold);
  }

  .plan-body {
    width: 100%;
    font-size: 1rem;
    line-height: 1.3rem;
    display: inline-flex;
    letter-spacing: 1.67px;
    color: var(--color-black);
    text-transform: uppercase;
    font-weight: var(--weight-bold);
  }

  .plan {
    display: flex;
    flex-flow: column nowrap;
    margin-bottom: 2.45rem;
  }

  .plan:nth-child(2) {
    margin-left: 6.8rem;
  }
  .plan:nth-child(3) {
    margin-left: 8rem;
  }

  .plan__name {
    opacity: .50;
    margin-bottom: .8rem;
  }

  .table-row:not(:last-of-type) {
    margin-bottom: 2.3rem;
  }

  .plan__check {
    opacity: 0;
  }
  .plan__check.checked {
    opacity: 1;
  }
</style>
