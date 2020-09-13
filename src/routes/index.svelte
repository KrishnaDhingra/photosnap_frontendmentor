<script>
	import PageTransition from '../components/PageTransition.svelte';
	import HomeHero from '../components/page_components/HomeHero.svelte';
	import HomeSec from '../components/page_components/HomeSec.svelte';

  const secTwoConfig = {
    left: false,
    secName: 'designed',
    heading: 'Designed for<br>everyone',
    body: 'Photosnap can help you create stories that resonate with your audience.  Our tool is designed for photographers of all levels, brands, businesses you name it.'
  }
</script>
<style>

</style>

<svelte:head>
	<title>Photosnap | Home | Frontend Mentor</title>
</svelte:head>

<PageTransition>
  <HomeHero/>
  <HomeSec/>
  <HomeSec sectionConfig={secTwoConfig} />

  The Mountains
  by John Appleseed
  Read Story

  Sunset Cityscapes
  by Benjamin Cruz
  Read Story

  18 Days Voyage
  by Alexei Borodin
  Read Story

  Architecturals
  by Samantha Brooke
  Read Story

  100% Responsive

  No matter which the device you’re on, our site is fully responsive and stories 
  look beautiful on any screen.

  No Photo Upload Limit

  Our tool has no limits on uploads or bandwidth. Freely upload in bulk and 
  share all of your stories in one go.

  Available to Embed

  Embed Tweets, Facebook posts, Instagram media, Vimeo or YouTube videos, 
  Google Maps, and more. 
</PageTransition>