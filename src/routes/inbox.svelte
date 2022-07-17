<script>
	import Button from '../components/button.svelte';

	import MailIcon from '../svgs/mail.svg.svelte';
	import InfoCircleIcon from '../svgs/info-circle.svg.svelte';
	import ArchiveIcon from '../svgs/archive.svg.svelte';
	import Searchicon from '../svgs/search.svg.svelte';

	let tags = ['All', 'Favourites', 'Science', 'Math', 'Economics'];
</script>

<main>
	<section class="toolbar">
		<Button text="Manage" imageAlt="mail icon" type="pill">
			<MailIcon slot="icon" />
		</Button>
		<div class="spacer" />
		<Button imageAlt="help icon" type="circle">
			<InfoCircleIcon slot="icon" />
		</Button>
		<div class="spacer" />
		<Button imageAlt="archive icon" type="circle">
			<ArchiveIcon slot="icon" />
		</Button>
		<div class="spacer" />
		<Button imageAlt="search icon" type="circle">
			<Searchicon slot="icon" />
		</Button>
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
		padding: var(--size-2) var(--size-3);
		position: relative;
	}

	section > .spacer {
		width: var(--size-3);
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
		padding: var(--size-1) var(--size-2);
		color: var(--text1);
	}
</style>
