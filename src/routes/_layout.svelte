<script>
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';

	export let segment;
</script>


<Navbar {segment}/>

<main>
	<slot></slot>
</main>

<Footer/>