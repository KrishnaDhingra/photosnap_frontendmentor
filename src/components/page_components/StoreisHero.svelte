<section class="hero">
  <div class="hero__image"></div>
  <div class="hero__content">
    <p class="t-subheading t-white">Last month's featured story</p>
    <h1 class="t-heading t-white hero__content__heading">Hazy full moon of Appalachia</h1>
    <div class="story__info">
      <p class="story__info__date t-storyinfo t-op75 t-white">March 2nd 2020</p>
      <p class="t-storyinfo t-white">by John Appleseed</p>
    </div>
    <p class="t-body t-white t-op6 story__body">The dissected plateau area, while not actually made up of geological mountains, 
    is popularly called "mountains," especially in eastern Kentucky and West Virginia, 
    and while the ridges are not high, the terrain is extremely rugged.</p>
    <a class="button button-cta button-cta--white t-white" href="/">Read the story</a>
  </div>
</section>

<style>
  @media (min-width: 768px) {
    .hero {
      position: relative;
    }
  }

  @media (min-width: 768px) {
    .hero::before {
      top: 0;
      left: 0;
      bottom: 0;
      width: 50%;
      content: '';
      position: absolute;
      /* opacity: 0.49; */
      background-image: radial-gradient(0% 35%, #FFC593 0%, rgba(188,113,152,0.50) 38%, rgba(90,119,255,0.00) 73%);
    }
  }

  .hero__image {
    width: 100%;
    height: 31.7rem;
    background-size: cover;
    background-repeat: no-repeat;
    background-image: url(/images/stories/mobile/moon-of-appalacia.jpg);
  }
  @media (min-width: 768px) {
    .hero__image {
      height: 65rem;
      background-image: url(/images/stories/tablet/moon-of-appalacia.jpg);
    }
  }
  @media (min-width: 1024px) {
    .hero__image {
      background-image: url(/images/stories/desktop/moon-of-appalacia.jpg);
    }
  }

  .hero__content {
    padding: 4.8rem 2.8rem 4.8rem 2.9rem;
    background-color: var(--color-black);
  }
  @media (min-width: 768px) {
    .hero__content {
      top: 50%;
      padding: 0;
      left: 5.078%;
      width: 38.7rem;
      background: none;
      position: absolute;
      transform: translateY(-50%);
    }
  }
  @media (min-width: 1024px) {
    .hero__content {
      left: 7.778%;
    }
  }

  .hero__content__heading {
    margin-top: 1.6rem;
    margin-bottom: 1.6rem;
  }

  .story__info {
    display: inline-flex;
  }

  .story__info__date {
    margin-right: .8rem;
  }

  .story__body {
    margin: 2.4rem 0;
  }

  


</style>