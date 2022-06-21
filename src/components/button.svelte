<script lang="ts">
	export let text: string = '';
	export let imageSource: string;
	export let imageAlt: string;
	export let type: 'pill' | 'circle' | 'oblong' = 'circle';
</script>

{#if type === 'circle'}
	<button class="round">
		<img src={imageSource} alt={imageAlt} class="icon" />
	</button>
{:else if type === 'pill'}
	<button class="pill">
		<img src={imageSource} alt={imageAlt} class="icon" />
		<div class="spacer" />
		<p>{text}</p>
	</button>
{/if}

<style>
	button {
		--dimension: 1.5rem;
		--normal-bg-color: var(--fill-gray);
		--hover-bg-color: var(--gray-5);

		background-color: var(--normal-bg-color);
		position: relative;
		transition: background-color 0.2s ease-in;
	}

	button:hover {
		background-color: var(--hover-bg-color);
	}

	button > p {
		font-size: var(--font-size-0);
		color: var(--text1);
	}

	button > .icon {
		height: 1rem;
		width: 1rem;
	}

	.pill {
		height: var(--dimension);
		display: flex;
		align-items: center;
		margin: 0 calc(var(--dimension) / 3);
	}

	.pill > .spacer {
		width: 4px;
	}

	.pill::before {
		position: absolute;
		content: '';
		height: var(--dimension);
		width: var(--dimension);
		left: calc(-1 * var(--dimension) / 3);
		background-color: var(--normal-bg-color);
		border-radius: var(--radius-round);
		z-index: -1;
		transition: background-color 0.2s ease-in;
	}
	.pill::after {
		position: absolute;
		content: '';
		height: var(--dimension);
		width: var(--dimension);
		right: calc(-1 * var(--dimension) / 3);
		background-color: var(--normal-bg-color);
		border-radius: var(--radius-round);
		z-index: -1;
		transition: background-color 0.2s ease-in;
	}

	button:hover::before,
	button:hover::after {
		background-color: var(--hover-bg-color);
	}

	.round {
		border-radius: var(--radius-round);
	}
</style>
