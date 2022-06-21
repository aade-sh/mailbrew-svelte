<nav>
	<ul>
		<li>
			<a href="/brews">
				<img src="/images/brew.svg" alt="Icon representing brews" />
				<div class="spacer" />
				<p>Brews</p>
			</a>
		</li>
		<li>
			<a href="/inbox">
				<img src="/images/inbox.svg" alt="Icon representing your inbox" />
				<div class="spacer" />
				<p>Newsletters</p>
			</a>
		</li>
		<li>
			<a href="/saved">
				<img src="/images/saved.svg" alt="Icon representing saved stuff" />
				<div class="spacer" />
				<p>Saved</p>
			</a>
		</li>
	</ul>
</nav>

<style>
	nav {
		display: flex;
		justify-content: space-around;
		padding: 0.4rem 0;
		border-bottom: var(--border-size-1) solid var(--gray-3);
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
		padding: 0.4rem 0.4rem;
		text-decoration: none;
		color: inherit;
		font-weight: var(--font-weight-4);
		border-radius: var(--radius-conditional-2);

		transition: background-color 0.2s ease-in;
	}

	li a:hover {
		background-color: var(--gray-3);
	}

	li .spacer {
		width: 0.2rem;
	}

	li img {
		height: 15px;
		width: 15px;
	}
</style>
