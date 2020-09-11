<script>
  import { createEventDispatcher } from 'svelte';
  let active = false;

  const dispatch = createEventDispatcher();

	const toggleMobileNav = () => {
    active = !active;
    dispatch('headerStatus', {
			status: active
		});
  };
</script>

<button on:click={toggleMobileNav} class="button button--burger">
  <svg class="menu{active ? ' active' : ''}" xmlns="http://www.w3.org/2000/svg" width="20" height="6"><g fill-rule="evenodd"><path d="M0 0h20v1H0zM0 5h20v1H0z"/></g></svg>
  <svg class="close{active ? ' active' : ''}" xmlns="http://www.w3.org/2000/svg" width="16" height="15"><path fill-rule="evenodd" d="M14.718.075l.707.707L8.707 7.5l6.718 6.718-.707.707L8 8.207l-6.718 6.718-.707-.707L7.293 7.5.575.782l.707-.707L8 6.793 14.718.075z"/></svg>
</button>

<style>
.button--burger {
  width: 2rem;
  height: 2rem;
  cursor: pointer;
  position: relative;
  display: inline-block;
}

.menu,
.close {
  top: 50%;
  left: 50%;
  position: absolute;
  transition: var(--transition) opacity, var(--transition) transform;
}

.menu {
  opacity: 1;
  transform: translate(-50%, -50%);
}

.close {
  opacity: 0;
  transform: translate(-50%, -50%) rotate(90deg);
  
}

.close.active {
  opacity: 1;
  transform: translate(-50%, -50%) rotate(0);
}

.menu.active {
  opacity: 0;
  transform: translate(-50%, -50%) rotate(90deg);
}


</style>