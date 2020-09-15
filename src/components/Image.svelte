<script>
  export let imageName
  export let alt
  import { onMount } from 'svelte'
  let loaded = false
  let thisImage
  onMount(() => {
    thisImage.onload = () => {
      loaded = true
    }
  }) 
</script>

<picture class:loaded>
  <source
    srcset="/images/stories/desktop/{imageName}.jpg"
    media="(min-width: 560px)"
  />
  <img class:loaded bind:this={thisImage} src="/images/stories/mobile/{imageName}.jpg" {alt}>
</picture>

<style>
  img {
    opacity: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
    transition: opacity 700ms ease-out;
  }
  img.loaded {
    opacity: 1;
  }

  picture::before {
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    content: '';
    position: absolute;
    background-image: linear-gradient(180deg, rgba(0,0,0,0.00) 0%, rgba(0,0,0,0.66) 100%);
  }

  picture {
    opacity: 0;
    display: flex;
    height: 37.5rem;
    position: relative;
    transition: opacity 1200ms ease-out;
  }
  picture.loaded {
    opacity: 1;
  }
  @media (min-width: 560px) {
    picture {
      height: 50rem;
    }
  }

</style>