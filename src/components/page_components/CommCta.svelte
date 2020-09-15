<section class="cta">
  <div class="container">
    <h2 class="t-heading t-white cta__heading">We're in Beta. Get your invite today!</h2>
    <a class="button button-cta button-cta--white t-white" href="/">Get an invite</a>
  </div>
</section>

<style>
  .cta {
    height: 28.8rem;
    position: relative;
    background-size: cover;
    background-repeat: no-repeat;
    background-image: url(/images/shared/mobile/bg-beta.jpg);
  }
  @media (min-width: 660px) {
    .cta {
      display: flex;
      height: 28rem;
      align-items: center;
      padding-right: 4rem;
      padding-left: 3.9rem;
      background-image: url(/images/shared/tablet/bg-beta.jpg);
    }
  }
  @media (min-width: 1024px) {
    .cta {
      background-image: url(/images/shared/desktop/bg-beta.jpg);
    }
  }

  .cta::before {
    top: 0;
    content: '';
    left: 3.3rem;
    height: .6rem;
    width: 12.8rem;
    position: absolute;
    background-image: linear-gradient(27deg, #FFC593 0%, #BC7198 49%, #5A77FF 95%);
  }
  @media (min-width: 660px) {
    .cta::before {
      left: 0;
      width: .6rem;
      height: 100%;
    }
  }

  .container {
    padding: 6.4rem 3.2rem 6.4rem 3.3rem;
  }
  @media (min-width: 660px) {
    .container {
      width: 100%;
      display: flex;
      margin: 0 auto;
      max-width: 111rem;
      padding: 6.8rem 0;
      justify-content: space-between;
    }
  }

  .cta__heading {
    margin-bottom: 2.4rem;
  }
  @media (min-width: 660px) {
    .cta__heading {
      width: 55%;
      margin-bottom: 0;
      max-width: 40rem;
    }
  }

  @media (min-width: 660px) {
    .button-cta {
      max-width: 16.8rem;
    }
  }
</style>