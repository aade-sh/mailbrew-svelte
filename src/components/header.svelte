<script>
	import BrewSvg from '../svgs/brew.svg.svelte';
	import InboxSvg from '../svgs/inbox.svg.svelte';
	import SavedSvg from '../svgs/saved.svg.svelte';
</script>

<nav>
	<ul>
		<li>
			<a href="/brews">
				<!-- #TODO a11y -->
				<span class="icon">
					<BrewSvg />
				</span>
				<div class="spacer" />
				<p>Brews</p>
			</a>
		</li>
		<li>
			<a href="/inbox">
				<!-- #TODO a11y -->
				<span class="icon">
					<InboxSvg />
				</span>
				<div class="spacer" />
				<p>Newsletters</p>
			</a>
		</li>
		<li>
			<a href="/saved">
				<!-- #TODO a11y -->
				<span class="icon">
					<SavedSvg />
				</span>
				<div class="spacer" />
				<p>Saved</p>
			</a>
		</li>
	</ul>
</nav>

<style>
	.icon {
		height: var(--size-3);
		width: var(--size-3);
	}
	nav {
		display: flex;
		justify-content: space-around;
		padding: var(--size-2) 0;
		border-bottom: var(--border-size-1) solid var(--bg1);
		color: var(--text1);
	}
	ul {
		display: flex;
		padding: 0;
	}

	li {
		list-style: none;
	}
	li a {
		display: flex;
		align-items: center;
		padding: var(--size-2);
		text-decoration: none;
		color: inherit;
		font-weight: var(--font-weight-4);
		border-radius: var(--radius-conditional-2);

		transition: background-color 0.2s ease-in;
	}

	li a:hover {
		background-color: var(--bg1);
	}

	li .spacer {
		width: var(--size-1);
	}
</style>
