<section class="hero">
  <div class="hero__image"></div>
  <div class="hero__content">
    <div class="hero__content__wrap">
      <h1 class="t-heading t-white hero__content__heading">Create and share your photo Stories.</h1>
      <p class="t-body t-white t-op6 hero__content__body">Photosnap is a platform for photographers and visual storytellers. We make it 
      easy to share photos, tell stories and connect with others.</p>
      <a class="button button-cta button-cta--white t-white" href="/">Get an invite</a>
    </div>
  </div>
</section>

<style>
  .hero__image {
    width: 100%;
    height: 29.4rem;
    background-size: cover;
    background-image: url(/images/home/mobile/create-and-share.jpg);
  }
  @media (min-width: 560px) {
    .hero__image {
      height: 65rem;
      width: 35.547%;
      background-position: center;
      background-image: url(/images/home/tablet/create-and-share.jpg);
    }
  }
  @media (min-width: 1160px) {
    .hero__image {
      width: 57.639%;
      background-image: url(/images/home/desktop/create-and-share.jpg);
    }
  }

  .hero__content {
    padding: 0 2.4rem 7.2rem 3.3rem;
    background-color: var(--color-black);
  }
  @media (min-width: 560px) {
    .hero__content {
      padding: 0;
      display: flex;
      height: 65rem;
      width: 64.453%;
      align-items: center;
    }
  }
  @media (min-width: 1160px) {
    .hero__content {
      width: 42.361%;
    }
  }

  .hero__content__wrap {
    position: relative;
    padding-top: 7.2rem;
  }
  @media (min-width: 560px) {
    .hero__content__wrap {
      padding: 0 2.7rem;
    }
  }
  @media (min-width: 700px) {
    .hero__content__wrap {
      width: 100%;
      display: flex;
      padding: 0 5.4rem;
      align-items: center;
      flex-direction: column;
    }
  }

  .hero__content__wrap::before {
    top: 0;
    left: 0;
    content: '';
    height: .6rem;
    width: 12.8rem;
    position: absolute;
    background-image: linear-gradient(27deg, #FFC593 0%, #BC7198 49%, #5A77FF 95%);
  }
  @media (min-width: 560px) {
    .hero__content__wrap::before {
      width: .6rem;
      height: 100%;
    }
  }

  .hero__content__body {
    margin-top: 1.6rem;
    margin-bottom: 2.3rem;
  }
  @media (min-width: 700px) {
    .hero__content__body {
      max-width: 38.7rem;
    }
  }

  .hero {
    display: flex;
    flex-flow: column nowrap;
  }
  @media (min-width: 560px) {
    .hero {
      flex-flow: row-reverse nowrap;
    }
  }

  @media (min-width: 700px) {
    .hero__content__heading {
      max-width: 38.7rem;
    }
  }
</style>