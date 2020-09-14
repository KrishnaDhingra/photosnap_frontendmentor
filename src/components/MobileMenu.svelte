<script>
  import { fade, fly } from 'svelte/transition';
  import { acitve } from './stores.js';
  
  let active_status;

  function updateActive() {
    acitve.update((ac) => ac = !ac);
  }

  const unsubscribe = acitve.subscribe(value => {
		active_status = value;
  });
  
</script>

{#if active_status}
<div on:click={updateActive} transition:fade class="full-screen-overlay">
  <div in:fly="{{ y: -200, duration: 700 }}" out:fade class="mobile-nav">
    <ul class="mobile-nav-menu">
      <li><a class="t-mobile-nav" href="stories">Stories</a></li>
      <li><a class="t-mobile-nav" href="features">Features</a></li>
      <li><a class="t-mobile-nav" href="pricing">Pricing</a></li>
    </ul>
    <a class="button button--cta-mobile t-button" href="/">Get an invite</a>
  </div>
</div>
{/if}

<style>
  .full-screen-overlay {
    top: 7.2rem;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 2;
    position: fixed;
    background-color: rgba(0, 0, 0, .50);
  }
  @media (min-width: 768px) {
    .full-screen-overlay {
      display: none;
    }
  }

  .mobile-nav {
    left: 0;
    right: 0;
    top: 7.2rem;
    width: 100%;
    position: fixed;
    padding: 3.2rem 0;
    text-align: center;
    background-color: var(--color-white);
  }
  @media (min-width: 768px) {
    .mobile-nav {
      display: none;
    }
  }

  .mobile-nav-menu {
    margin: 0 auto;
    width: 82.667%;
    text-align: center;
    border-bottom: 1px solid rgba(0, 0, 0, .25);
  }

  .mobile-nav-menu > li {
    margin-bottom: 2rem;
  }

  .button--cta-mobile {
    width: 82.667%;
    margin-top: 2rem;
    padding: 1.4rem 0;
    justify-content: center;
    color: var(--color-white);
    background-color: var(--color-black);
  }
</style>