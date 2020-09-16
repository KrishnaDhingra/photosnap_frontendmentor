<script>
	import PageTransition from '../components/PageTransition.svelte';
  import CommHero from '../components/page_components/CommHero.svelte';
  import PricingOptions from '../components/page_components/PricingOptions.svelte';
  import PricingTable from '../components/page_components/PricingTable.svelte';
  import CommCta from '../components/page_components/CommCta.svelte';
</script>

<svelte:head>
	<title>Photosnap | Pricing | Frontend Mentor</title>
</svelte:head>

<PageTransition>
  <CommHero
		heading={'Pricing'}
		pageName={'pricing'}
		subheading={'Create a your stories, Photosnap is a platform for photographers and visual storytellers. It’s the simple way to create and share your photos.'}
	/>
  <PricingOptions/>
  <PricingTable/>
  <CommCta/>
</PageTransition>