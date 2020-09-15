<script>
  export let heading
  export let subheading
  export let pageName
</script>

<section class="hero">
  <picture class="hero__image">
    <source
      srcset="/images/{pageName}/desktop/hero.jpg"
      media="(min-width: 1024px)"
    />
    <source
      srcset="/images/{pageName}/tablet/hero.jpg"
      media="(min-width: 560px)"
    />
    <img src="/images/{pageName}/mobile/hero.jpg" alt="hero">
  </picture>
  <div class="hero__content">
    <div class="hero__content-wrap">
      <h1 class="t-heading t-white">{heading}</h1>
      <p class="hero__subheading t-body t-white t-op6">{subheading}</p>
    </div>
  </div>
</section>

<style>
  img {
    width: 100%;
    object-fit: cover;
  }

  picture {
    display: flex;
    height: 29.4rem;
  }
  @media (min-width: 560px) {
    picture {
      height: 49rem;
    }
  }

  @media (min-width: 560px) {
    .hero {
      display: flex;
      flex-flow: row-reverse nowrap;
    }
  }

  @media (min-width: 560px) {
    .hero__image {
      width: 35.547%;
    }
  }
  @media(min-width: 1024px) {
    .hero__image {
      width: 57.639%;
    }
  }

  .hero__content {
    padding: 0 2.8rem 7.2rem 2.9rem;
    background-color: var(--color-black);
  }
  @media (min-width: 560px) {
    .hero__content {
      padding: 0;
      display: flex;
      width: 64.453%;
      align-items: center;
    }
  }
  @media(min-width: 1024px) {
    .hero__content {
      width: 42.361%;
    }
  }

  .hero__content-wrap {
    position: relative;
    padding-top: 7.2rem;
  }
  @media (min-width: 560px) {
    .hero__content-wrap {
      padding-top: 0;
      padding: 0 10.91%;
    }
  }
  @media (min-width: 1366px) {
    .hero__content-wrap {
      padding: 0 18.35%;
    }
  }

  .hero__content-wrap::before {
    content: '';
    top: 0;
    left: 0;
    height: .6rem;
    width: 12.8rem;
    position: absolute;
    background-image: linear-gradient(27deg, #FFC593 0%, #BC7198 49%, #5A77FF 95%);
  }
  @media (min-width: 560px) {
    .hero__content-wrap::before {
      width: .6rem;
      height: 100%;
    }
  }

  .hero__subheading {
    margin-top: 1.6rem;
  }
  @media (min-width: 560px) {
    .hero__subheading {
      margin-top: 2.1rem;
    }
  }
</style>