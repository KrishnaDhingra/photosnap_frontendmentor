<script>
	import PageTransition from '../components/PageTransition.svelte';
	import HomeHero from '../components/page_components/HomeHero.svelte';
	import HomeSec from '../components/page_components/HomeSec.svelte';
	import HomeGallery from '../components/page_components/HomeGallery.svelte';
	import HomeFeatures from '../components/page_components/HomeFeatures.svelte';

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
  <HomeGallery/>
  <HomeFeatures/>
</PageTransition>