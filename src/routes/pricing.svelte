<script>
	import PageTransition from '../components/PageTransition.svelte';
  import CommHero from '../components/page_components/CommHero.svelte';
  import PricingOptions from '../components/page_components/PricingOptions.svelte';
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

  Compare

  The Features

  Basic
  Pro
  Business

  Unlimited Story Posting
  Unlimited Photo Upload
  Embedding Custom Content
  Customize Metadata
  Advanced Metrics
  Photo Downloads
  Search Engine Indexing
  Custom Analytics

  <CommCta/>
</PageTransition>