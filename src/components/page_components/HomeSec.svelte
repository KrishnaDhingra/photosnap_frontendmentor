<script>
  export let sectionConfig = {
    left: true,
    secName: 'stories',
    heading: 'Beautiful stories<br> every time',
    body: 'We provide design templates to ensure your stories look terrific. Easily add photos, text, embed maps and media from other networks. Then share your story with everyone.'
  };

</script>

<section class="homesec {sectionConfig.left ? 'left' : 'right'}">
  <div class="homesec__image homesec__image--{sectionConfig.secName}"></div>
  <div class="homesec__content">
    <div class="homesec__content__wrap homesec__content__wrap--{sectionConfig.secName}">
      <h1 class="t-heading t-black homesec__content__heading">{@html sectionConfig.heading}</h1>
      <p class="t-body t-black t-op6 homesec__content__body">{sectionConfig.body}</p>
      <a class="button button-cta button-cta--black t-black" href="/">View the stories</a>
    </div>
  </div>
</section>

<style>
  .homesec__image {
    width: 100%;
    height: 27.1rem;
    background-size: cover;
  }
  @media (min-width: 578px) {
    .homesec__image {
      width: 35.547%;
      height: 60rem;
    }
  }
  @media (min-width: 1024px) {
    .homesec__image {
      width: 57.639%;
    }
  }

  @media (min-width: 578px) {
    .homesec {
      display: flex;
    }
    .homesec.left {
      flex-flow: row nowrap;
    }
    .homesec.right {
      flex-flow: row-reverse nowrap;
    }
  }

  @media (min-width: 578px) {
    .homesec__content {
      width: 64.453%;
      display: flex;
      align-items: center;
      flex-flow: row nowrap;
      justify-content: center;
    }
  }
  @media (min-width: 1024px) {
    .homesec__content {
      width: 42.361%;
    }
  }

  .homesec__image--stories {
    background-image: url(/images/home/mobile/beautiful-stories.jpg);
  }
  @media (min-width: 578px) {
    .homesec__image--stories {
      background-image: url(/images/home/tablet/beautiful-stories.jpg);
    }
  }
  @media (min-width: 1024px) {
    .homesec__image--stories {
      background-image: url(/images/home/desktop/beautiful-stories.jpg);
    }
  }
  .homesec__image--designed {
    background-image: url(/images/home/mobile/designed-for-everyone.jpg);
  }
  @media (min-width: 578px) {
    .homesec__image--designed {
      background-image: url(/images/home/tablet/designed-for-everyone.jpg);
    }
  }
  @media (min-width: 1024px) {
    .homesec__image--designed {
      background-image: url(/images/home/desktop/designed-for-everyone.jpg);
    }
  }

  .homesec__content__wrap {
    padding-left: 3.3rem;
    padding-right: 2.4rem;
  }
  @media (min-width: 578px) {
    .homesec__content__wrap {
      padding-left: 0;
      padding-right: 0;
      width: 78.182%;
    }
  }
  @media (min-width: 1280px) {
    .homesec__content__wrap {
      width: 63.443%;
    }
  }

  .homesec__content__wrap--stories {
    padding-top: 7.2rem;
    padding-bottom: 7.2rem;
  }
  @media (min-width: 578px) {
    .homesec__content__wrap--stories {
      padding-top: 0;
      padding-bottom: 0;
    }
  }
  
  .homesec__content__wrap--designed {
    padding-top: 9.2rem;
    padding-bottom: 9.2rem;
  }
  @media (min-width: 578px) {
    .homesec__content__wrap--designed {
      padding-top: 0;
      padding-bottom: 0;
    }
  }
  

  .homesec__content__body {
    margin-top: 1.6rem;
    margin-bottom: 2.3rem;
  }
  @media (min-width: 578px) {
    .homesec__content__body {
      margin-top: 2.1rem;
      margin-bottom: 4.8rem;
    }
  }
</style>