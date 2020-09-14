<div class="socials">
  <a class="social social--facebook" href="/" target="_blank">
    <span class="sr-only">social link</span>
  </a>
  <a class="social social--youtube" href="/" target="_blank">
    <span class="sr-only">social link</span>
  </a>
  <a class="social social--twitter" href="/" target="_blank">
    <span class="sr-only">social link</span>
  </a>
  <a class="social social--pinterest" href="/" target="_blank">
    <span class="sr-only">social link</span>
  </a>
  <a class="social social--instagram" href="/" target="_blank">
    <span class="sr-only">social link</span>
  </a>
</div>

<style>
  .socials {
    width: 15.4rem;
    display: inline-flex;
    margin-bottom: 4.9rem;
    justify-content: space-between;
  }
  @media (min-width: 700px) {
    .socials {
      grid-row: 3/4;
      grid-column: 1/2;
      margin-bottom: 0;
    }
  }
  @media (min-width: 1024px) {
    .socials {
      grid-row: 2/3;
      grid-column: 1/2;
    }
  }

  .social {
    width: 2rem;
    height: 2rem;
    cursor: pointer;
    display: inline-flex;
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    transition: var(--transition) background, var(--transition) transform;
  }

  .social:hover {
    transform: scale(1.1);
  }


  .social--facebook {
    background-image: url(/images/shared/desktop/facebook.svg);
  }
  .social--facebook:hover {
    background-image: url(/images/shared/desktop/facebook-hover.svg);
  }
  .social--youtube {
    background-image: url(/images/shared/desktop/youtube.svg);
  }
  .social--youtube:hover {
    background-image: url(/images/shared/desktop/youtube-hover.svg);
  }
  .social--twitter {
    background-image: url(/images/shared/desktop/twitter.svg);
  }
  .social--twitter:hover {
    background-image: url(/images/shared/desktop/twitter-hover.svg);
  }
  .social--pinterest {
    background-image: url(/images/shared/desktop/pinterest.svg);
  }
  .social--pinterest:hover {
    background-image: url(/images/shared/desktop/pinterest-hover.svg);
  }
  .social--instagram {
    background-image: url(/images/shared/desktop/instagram.svg);
  }
  .social--instagram:hover {
    background-image: url(/images/shared/desktop/instagram-hover.svg);
  }


</style>