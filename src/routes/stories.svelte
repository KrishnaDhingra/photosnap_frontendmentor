<script>
	import PageTransition from '../components/PageTransition.svelte';
	import StoriesHero from '../components/page_components/StoriesHero.svelte';
	import StoriesGallery from '../components/page_components/StoriesGallery.svelte';
</script>

<svelte:head>
	<title>Photosnap | Stories | Frontend Mentor</title>
</svelte:head>

<PageTransition>
	<StoriesHero/>
	<StoriesGallery/>
</PageTransition>