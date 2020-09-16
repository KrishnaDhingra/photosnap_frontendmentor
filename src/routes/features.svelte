<script>
	import PageTransition from '../components/PageTransition.svelte';
	import CommHero from '../components/page_components/CommHero.svelte';
	import FeaturesList from '../components/page_components/FeaturesList.svelte';
	import CommCta from '../components/page_components/CommCta.svelte';
	
</script>

<svelte:head>
	<title>Photosnap | Features | Frontend Mentor</title>
</svelte:head>

<PageTransition>
	<CommHero
		heading={'Features'}
		pageName={'features'}
		subheading={'We make sure all of our features are designed to be loved by every aspiring and even professional photograpers who wanted to share their stories.'}
	/>
	<FeaturesList/>
	<CommCta/>
</PageTransition>