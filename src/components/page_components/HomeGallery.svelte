<script>
  const photos = [
    { name: 'The Mountains', img:'mountains', photographer: 'John Appleseed', link: '/stories' },
    { name: 'Sunset Cityscapes', img:'cityscapes', photographer: 'Benjamin Cruz', link: '/stories' },
    { name: '18 Days Voyage', img:'18-days-voyage', photographer: 'Alexei Borodin', link: '/stories' },
    { name: 'Architecturals', img:'architecturals', photographer: 'Samantha Brooke', link: '/stories' },
  ]
</script>

<section class="gallery">
  {#each photos as photo}
    <a class="photo" href="{photo.link}">
      <picture>
        <source
          srcset="/images/stories/desktop/{photo.img}.jpg"
          media="(min-width: 560px)"
        />
        <img src="/images/stories/mobile/{photo.img}.jpg" alt="story">
      </picture>
      <div class="photo__detail">
        <p class="photo__detail__name t-white t-photoname">{photo.name}</p>
        <p class="photo__detail__photographer t-white t-photographer">by {photo.photographer}</p>
        <div class="divider"></div>
        <p class="button button--story t-white">Read Story</p>
      </div>
    </a>
  {/each}
</section>

<style>
  picture {
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    position: absolute;
  }

  picture img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
  }
  @media (min-width: 560px) {
    picture img {
      object-position: center;
    }
  }

  .gallery {
    display: grid;
  }
  @media (min-width: 560px) {
    .gallery {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  @media (min-width: 1024px) {
    .gallery {
      grid-template-columns: repeat(4, 1fr);
    }
  }

  .photo {
    width: 100%;
    display: block;
    height: 37.5rem;
    cursor: pointer;
    position: relative;
    transition: var(--transition) transform;
  }
  @media (min-width: 560px) {
    .photo {
      height: 50rem;
    }
  }

  .photo:hover {
    transform: translateY(-2.4rem);
  }

  .photo::before {
    left: 0;
    right: 0;
    bottom: 0;
    height: 0;
    z-index: 3;
    opacity: 0;
    content: '';
    position: absolute;
    transition: var(--transition) height, var(--transition) opacity;
    background-image: linear-gradient(27deg, #FFC593 0%, #BC7198 49%, #5A77FF 95%);
  }
  .photo:hover::before {
    opacity: 1;
    height: .6rem;
  }

  .photo::after {
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    content: '';
    position: absolute;
    background-image: linear-gradient(180deg, rgba(0,0,0,0.00) 0%, rgba(0,0,0,0.66) 100%);
  }

  .photo__detail {
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 2;
    position: absolute;
    padding: 0 3.2rem 4rem 3.3rem;
  }
  @media (min-width: 768px) {
    .photo__detail {
      padding: 0 4.278rem 4rem 4.322rem;
    }
  }
  @media (min-width: 1024px) {
    .photo__detail {
      padding: 0 2.4rem 4rem;
    }
  }
  @media (min-width: 1200px) {
    .photo__detail {
      padding: 0 4rem 4rem;
    }
  }

  .divider {
    width: 100%;
    opacity: .25;
    height: .1rem;
    margin: 1.6rem 0 2rem;
    background-color: var(--color-white);
  }
  
  .button--story {
    width: 100%;
    font-size: 1.2rem;
    letter-spacing: 2px;
    line-height: 1.6rem;
    display: inline-flex;
    text-transform: uppercase;
    justify-content: space-between;
    font-weight: var(--weight-bold);
  }
  .button--story::after {
    content: '';
    width: 4.2rem;
    height: 1.2rem;
    background-size: cover;
    background-image: url(/images/shared/desktop/arrow-white.svg);
  }

  .photo__detail__photographer {
    margin-top: .4rem;
  }
</style>