<script>
  let active = false;
</script>

<section class="pricing">
  <div class="container">
    <div class="switcher-container">
      <span class="t-switcher{active ? ' active': ''}">Monthly</span>
      <div on:click="{() => active = !active}" class:active class="switcher"></div>
      <span class="t-switcher{!active ? ' active': ''}" >Yearly</span>
    </div>
    <div class="options-container">
      <div class="option option--gray">
        <h3 class="t-option-heading t-black">Basic</h3>
        <p class="t-body t-black t-op6 option__detail">Includes basic usage of our platform. Recommended for new and aspiring photographers.</p>
        <div class="option__price">
        {#if !active}
          <p class="t-price t-black">$19.00</p>
          <p class="t-body t-black t-op6 option__price__per">per month</p>
        {:else}
          <p class="t-price t-black">$190.00</p>
          <p class="t-body t-black t-op6 option__price__per">per year</p>
        {/if}
        </div>
        <a class="button button--plan button-black t-pickplan t-white" href="/">Pick Plan</a>
      </div>
      
      <div class="option option--black">
        <h3 class="t-option-heading t-white">Pro</h3>
        <p class="t-body t-white t-op6 option__detail">More advanced features available. Recommended for photography veterans and professionals.</p>
        <div class="option__price">
        {#if !active}
          <p class="t-price t-white">$39.00</p>
          <p class="t-body t-white t-op6 option__price__per">per month</p>
        {:else}
          <p class="t-price t-white">$390.00</p>
          <p class="t-body t-white t-op6 option__price__per">per year</p>
        {/if}
        </div>
        <a class="button button--plan button-white t-pickplan t-black" href="/">Pick Plan</a>
      </div>

      <div class="option option--gray">
        <h3 class="t-option-heading t-black">Business</h3>
        <p class="t-body t-black t-op6 option__detail">Additional features available such as more detailed metrics. Recommended for business owners.</p>
        <div class="option__price">
        {#if !active}
          <p class="t-price t-black">$99.00</p>
          <p class="t-body t-black t-op6 option__price__per">per month</p>
        {:else}
          <p class="t-price t-black">$990.00</p>
          <p class="t-body t-black t-op6 option__price__per">per year</p>
        {/if}
        </div>
        <a class="button button--plan button-black t-pickplan t-white" href="/">Pick Plan</a>
      </div>
    </div>
  </div>
</section>

<style>
  .switcher {
    width: 6.4rem;
    height: 3.2rem;
    cursor: pointer;
    margin: 0 3.2rem;
    align-items: center;
    display: inline-flex;
    border-radius: 1.6rem;
    justify-content: flex-start;
    background-color: var(--color-gray);
    transition: var(--transition) background-color, 360ms cubic-bezier(1.000, 0.075, 0.530, 0.910) transform;
  }

  .switcher:hover {
    transform: scale(1.2);
  }

  .switcher::after {
    content: '';
    width: 2.4rem;
    height: 2.4rem;
    border-radius: 50%;
    margin-left: .4rem;
    background-color: var(--color-black);
    transition: var(--transition) background-color, var(--transition) margin;
  }

  .switcher.active {
    background-color: var(--color-black);
  }

  .switcher.active::after {
    margin-left: auto;
    margin-right: .4rem;
    background-color: var(--color-white);
  }

  .switcher-container {
    align-items: center;
    display: inline-flex;
  }

  .t-switcher {
    color: var(--color-black);
    transition: var(--transition) opacity;
  }

  .t-switcher.active {
    opacity: .50;
  }



  .container {
    text-align: center;
    padding: 6.4rem 2.8rem 6.4rem 2.9rem;
  }
  @media (min-width: 768px) {
    .container {
      margin: 0 auto;
      max-width: 111rem;
      padding: 11.2rem 0;
    }
  }
  @media (min-width: 768px) {
    .container {
      padding: 12rem 0 16rem;
    }
  }

  @media (min-width: 768px) {
    .pricing {
      padding-right: 4rem; 
      padding-left: 3.9rem;
    }
  }
  @media (min-width: 920px) {
    .pricing {
      padding-right: 16rem; 
      padding-left: 16rem;
    }
  }
  @media (min-width: 1200px) {
    .pricing {
      padding: 0;
    }
  }

  .option--gray {
    background-color: #F5F5F5;
    padding: 5.6rem 2.2rem 4rem 2.1rem;
  }
  @media (min-width: 768px) {
    .option--gray {
      padding: 0;
    }
  }
  

  .option--black {
    position: relative;
    background-color: var(--color-black);
    padding: 4.8rem 2.2rem 4.8rem 2.1rem;
  }
  @media (min-width: 768px) {
    .option--black {
      padding: 0;
    }
  }
 

  .option--black::before {
    top: 0;
    left: 0;
    width: 100%;
    content: '';
    height: .6rem;
    position: absolute;
    background-image: linear-gradient(27deg, #FFC593 0%, #BC7198 49%, #5A77FF 95%);
  }
  @media (min-width: 768px) {
    .option--black::before {
      width: .6rem;
      height: 100%;
    }
  }
  @media (min-width: 1200px) {
    .option--black::before {
      width: 100%;
      height: .6rem;
    }
  }

  .option__detail {
    margin-top: 1.8rem;
    margin-bottom: 4rem;
  }
  @media (min-width: 768px) {
    .option__detail {
      grid-row: 2/3;
      grid-column: 1/2;
      text-align: left;
      max-width: 27rem;
      margin-bottom: 3.2rem;
    }
  }
  @media (min-width: 1200px) {
    .option__detail {
      text-align: center;
      margin-bottom: 4rem;
    }
  }

  .option__price {
    display: flex;
    align-items: center;
    margin-bottom: 4rem;
    flex-flow: column nowrap;
  }
  @media (min-width: 768px) {
    .option__price {
      grid-row: 1/4;
      grid-column: 2/3;
      margin-bottom: 0;
      justify-self: end;
      align-items: flex-end;
    }
  }
  @media (min-width: 1200px) {
    .option__price {
      align-items: center;
      margin-bottom: 4rem;
    }
  }

  .options-container {
    display: grid;
    row-gap: 2.4rem;
    margin-top: 4rem;
  }
  @media (min-width: 1200px) {
    .options-container {
      row-gap: 0;
      column-gap: 3rem;
      align-items: center;
      grid-template-columns: repeat(3, 1fr);
    }
  }

  @media (min-width: 768px) {
    .option {
      display: grid;
      justify-items: start;
      grid-template-columns: repeat(2, 1fr);
      padding: 4rem 4.8rem 4rem 4rem;
    }
  }
  @media (min-width: 1200px) {
    .option {
      display: flex;
      flex-flow: column nowrap;
    }
  }

  @media (min-width: 768px) {
    .button--plan {
      grid-row: 3/4;
      grid-column: 1/2;
    }
  }

  @media (min-width: 768px) {
    .option__price__per {
      margin-right: .8rem;
    }
  }
  @media (min-width: 1200px) {
    .option__price__per {
      margin-right: 0;
    }
  }


  @media (min-width: 1200px) {
    .option--gray {
       padding: 5.6rem 4rem 4rem;
    }
  }
 @media (min-width: 1200px) {
    .option--black {
      padding: 8.8rem 4rem 7.1rem;
    }
  }
</style>