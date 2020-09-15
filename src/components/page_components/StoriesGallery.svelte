<script>
import ImageLoader from '../ImageLoader.svelte';

const stories = [
  {imageName: 'mountains', date: 'April 16th 2020', title: 'The Mountains', photographer: 'John Appleseed'},
  {imageName: 'cityscapes', date: 'April 14th 2020', title: 'Sunset Cityscapes', photographer: 'Benjamin Cruz'},
  {imageName: '18-days-voyage', date: 'April 11th 2020', title: '18 Days Voyage', photographer: 'Alexei Borodin'},
  {imageName: 'architecturals', date: 'April 9th 2020', title: 'Architecturals', photographer: 'Samantha Brooke'},
  {imageName: 'world-tour', date: 'April 7th 2020', title: 'World Tour 2019', photographer: 'Timothy Wagner'},
  {imageName: 'unforeseen-corners', date: 'April 3rd 2020', title: 'Unforeseen Corners', photographer: 'William Malcolm'},
  {imageName: 'king-on-africa', date: 'March 29th 2020', title: 'King on Africa: Part II', photographer: 'Tim Hillenburg'},
  {imageName: 'trip-to-nowhere', date: 'March 21st 2020', title: 'The Trip to Nowhere', photographer: 'Felicia Rourke'},
  {imageName: 'rage-of-the-sea', date: 'March 19th 2020', title: 'Rage of The Sea', photographer: 'Mohammed Abdul'},
  {imageName: 'running-free', date: 'March 16th 2020', title: 'Running Free', photographer: 'Michelle'},
  {imageName: 'behind-the-waves', date: 'March 11th 2020', title: 'Behind the Waves', photographer: 'Lamarr Wilson'},
  {imageName: 'calm-waters', date: 'March 9th 2020', title: 'Calm Waters', photographer: 'Samantha Brooke'},
  {imageName: 'milky-way', date: 'March 5th 2020', title: 'The Milky Way', photographer: 'Benjamin Cruz'},
  {imageName: 'dark-forest', date: 'March 4th 2020', title: 'Night at The Dark Forest', photographer: 'Mohammed Abdul'},
  {imageName: 'somwarpet', date: 'March 1st 2020', title: 'Somwarpet’s Beauty', photographer: 'Michelle'},
  {imageName: 'land-of-dreams', date: 'February 25th 2020', title: 'Land of Dreams', photographer: 'William Malcolm'}
];

</script>

<section class="stories">
  {#each stories as story}
    <a class="story" href="/">
      <ImageLoader imageName={story.imageName} alt="story"></ImageLoader>
      <div class="story__detail">
        <p class="story__detail__date t-white t-photographer">{story.date}</p>
        <p class="story__detail__title t-white t-photoname">{story.title}</p>
        <p class="story__detail__photographer t-white t-photographer">{story.photographer}</p>
        <div class="divider"></div>
        <p class="button button--story t-white">Read Story</p>
      </div>
    </a>
  {/each}
</section>

<style>
  .stories {
    display: grid;
  }
  @media (min-width: 560px) {
    .stories {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  @media (min-width: 1024px) {
    .stories {
      grid-template-columns: repeat(4, 1fr);
    }
  }

  .story {
    display: flex;
    position: relative;
    transition: var(--transition) transform;
  }

  .story::before {
    left: 0;
    width: 0;
    bottom: 0;
    z-index: 1;
    opacity: 0;
    content: '';
    height: .6rem;
    position: absolute;
    transition: var(--transition) opacity, var(--transition) width;
    background-image: linear-gradient(27deg, #FFC593 0%, #BC7198 49%, #5A77FF 95%);
  }
  .story:hover::before {
    opacity: 1;
    width: 100%;
  }

  .story:hover {
    transform: translateY(-2.4rem);
  }
  
  .story__detail {
    left: 0;;
    bottom: 0;
    width: 100%;
    position: absolute;
    padding-bottom: 4rem;
    padding-left: 4.167rem;
    padding-right: 4.133rem;
  }
  @media (min-width: 768px) {
    .story__detail {
      padding-bottom: 4rem;
      padding-left: 4.267rem;
      padding-right: 4.233rem;
    }
  }
  @media (min-width: 1024px) {
    .story__detail {
      padding-bottom: 2.4rem;
      padding-left: 2.4rem;
      padding-right: 2.4rem;
    }
  }
  @media (min-width: 1200px) {
    .story__detail {
      padding-bottom: 4rem;
      padding-left: 4rem;
      padding-right: 4rem;
    }
  }

  .story__detail__title {
    margin: .4rem 0;
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
</style>