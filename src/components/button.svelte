<script lang="ts">
	export let text: string = '';
	export let imageAlt: string;
	export let type: 'pill' | 'circle' | 'oblong' = 'circle';
</script>

{#if type === 'circle'}
	<button class="round">
		<span class="icon">
			<slot name="icon" />
		</span>
	</button>
{:else if type === 'pill'}
	<button class="pill">
		<span class="icon" aria-hidden="true">
			<slot name="icon" />
		</span>
		<div class="spacer" />
		<p>{text}</p>
	</button>
{/if}

<style>
	button {
		--dimension: var(--size-5);
		--normal-bg-color: var(--bg2);
		--hover-bg-color: var(--bg1);

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
		display: block;
		height: var(--size-3);
		width: var(--size-3);
	}

	.icon {
		color: var(--text1);
	}

	.pill {
		height: var(--dimension);
		display: flex;
		align-items: center;
		margin: 0 calc(var(--dimension) / 3);
	}

	.pill > .spacer {
		width: var(--size-1);
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
