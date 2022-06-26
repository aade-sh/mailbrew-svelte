<script>
	import Button from '../components/button.svelte';
</script>

<section class="brewSelector">
	<ul>
		<li>
			<button>
				<p class="name">Tech</p>
				<p class="published">8h ago</p>
			</button>
		</li>
		<li><button class="newBrew">+</button></li>
	</ul>
</section>
<section class="brewDetails">
	<h1>Tech</h1>
	<div class="issuePaginator">
		<button class="leftButton paginatorButton">
			<img src="/images/chevron-left.svg" alt="Go back" />
		</button>
		<span class="issueName">Issue #129</span>
		<button class="rightButton paginatorButton">
			<img src="/images/chevron-right.svg" alt="Go forward" />
		</button>
	</div>
	<ul class="brewOptions">
		<li>
			<Button type="pill" text="Edit" imageSource="/images/pencil.svg" imageAlt="Edit button" />
			<Button type="pill" text="Share" imageSource="/images/share.svg" imageAlt="Share button" />
			<Button
				type="pill"
				text="More"
				imageSource="/images/dots-horizontal.svg"
				imageAlt="More button"
			/>
		</li>
	</ul>
</section>

<style>
	/* brew selector */

	* {
		color: var(--text1);
	}

	.brewSelector {
		padding: var(--size-3) 0;
	}

	.brewSelector > ul {
		display: flex;
		gap: var(--size-3);
		align-items: stretch;
	}

	.brewSelector li button {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		padding: var(--size-2);

		border: var(--border-size-1) solid transparent;
		border-radius: var(--border-size-3);
	}

	/* brew details */

	.brewDetails {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: var(--size-3);
	}
	.brewOptions li {
		display: flex;
		gap: var(--size-3);
	}

	.issuePaginator {
		display: flex;
		align-items: center;
		gap: var(--size-2);
	}

	.issuePaginator .paginatorButton {
		height: var(--size-5);
		width: var(--size-5);
	}
</style>
