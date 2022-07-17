<script>
	import Header from '../components/header.svelte';
</script>

<Header />
<main>
	<slot />
</main>

<style global>
	html {
		--text1: var(--gray-8);
		--text2: var(--gray-7);

		--bg1: var(--gray-3);
		--bg2: var(--gray-1);

		--fill-gray: var(--gray-2);
	}

	@media (prefers-color-scheme: dark) {
		html {
			--text1: var(--gray-1);
			--text2: var(--gray-3);

			--bg1: var(--gray-7);
			--bg2: var(--gray-8);

			--fill-gray: var(--gray-8);
		}
	}
	main {
		margin: 0 auto;
		display: grid;
		place-items: center;
	}
</style>
