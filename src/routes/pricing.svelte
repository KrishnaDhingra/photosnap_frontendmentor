<script>
	import PageTransition from '../components/PageTransition.svelte';
  import CommHero from '../components/page_components/CommHero.svelte';
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
  

  Monthly
  Yearly

  Basic
  Includes basic usage of our platform. Recommended for new and aspiring photographers.
  $19.00 per month
  $190.00 per year
  Pick Plan

  Pro
  More advanced features available. Recommended for photography veterans and professionals.
  $39.00 per month
  $390.00 per year
  Pick Plan

  Business
  Additional features available such as more detailed metrics. Recommended for business owners.
  $99.00 per month
  $990.00 per year
  Pick Plan

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