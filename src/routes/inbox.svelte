<script>
	import Button from '../components/button.svelte';

	let tags = ['All', 'Favourites', 'Science', 'Math', 'Economics'];
</script>

<main>
	<section class="toolbar">
		<Button imageSource="/images/mail.svg" text="Manage" imageAlt="mail icon" type="pill" />
		<div class="spacer" />
		<Button imageSource="/images/information-circle.svg" imageAlt="help icon" type="circle" />
		<div class="spacer" />
		<Button imageSource="/images/archive.svg" imageAlt="archive icon" type="circle" />
		<div class="spacer" />
		<Button imageSource="/images/search.svg" imageAlt="search icon" type="circle" />
	</section>
	<section class="tagTabs">
		<ul>
			{#each tags as tag}
				<li>
					<button>{tag}</button>
				</li>
			{/each}
		</ul>
	</section>
</main>

<style>
	section {
		display: flex;
		padding: 0.5rem 1rem;
		position: relative;
	}

	section > .spacer {
		width: 1rem;
	}

	.tagTabs {
		padding: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		border-bottom: var(--border-size-1) solid var(--gray-3);
	}

	.tagTabs > ul {
		display: flex;
		list-style: none;
		text-decoration: none;
	}

	.tagTabs button {
		padding: 0.2rem 0.4rem;
	}
</style>
