<script>
	import Header from '../components/header.svelte';
</script>

<Header />
<main>
	<slot />
</main>

<style>
	main {
		margin: 0 auto;
		display: grid;
		place-items: center;
	}
</style>
