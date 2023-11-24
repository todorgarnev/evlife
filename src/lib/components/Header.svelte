<script lang="ts">
	import Logo from "$lib/assets/logo.png";

	const navItems = ["EV news", "EV ревюта", "EV masters"];
	const navItemsSoon = ["календар", "публикации"];
</script>

<header class="wrapper">
	<img src={Logo} alt="Carlife by Dani Logo" />

	<nav>
		<ul>
			{#each navItems as item, i}
				<li>
					<span>{String(i + 1).padStart(2, "0")}</span>
					<span>{item}</span>
				</li>
			{/each}

			{#each navItemsSoon as item}
				<li>
					<span>Скоро</span>
					<span class="soon text-gray">{item}</span>
				</li>
			{/each}
		</ul>
	</nav>

	<span>🔍</span>

	<span class="diagonal-line" />

	<div class="sidebar">
		<span>сподели с нас...</span>

		<div>
			<div>
				<span>Новини за EV NEWS</span>
				<span class="text-gray">Теми, които те вълнуват</span>
			</div>

			<div>
				<span>Твоята EV Кола</span>
				<span class="text-gray">Запиши колата си за ревю</span>
			</div>
		</div>
	</div>
</header>

<style>
	header {
		padding-block: 2rem;
		display: flex;
		align-items: center;
		background-color: var(--primary-bg-color);
		color: var(--font-color-white);
		border-top: 0.1rem solid var(--secondary-red-color);
	}

	img {
		margin-right: 4rem;
		width: 100%;
		max-width: 20rem;
		height: 100%;
	}

	nav {
		margin-right: auto;
	}

	nav ul {
		display: flex;
		gap: 2rem;
		text-transform: capitalize;
	}

	nav ul li {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
		cursor: pointer;
	}

	nav ul li span:first-child {
		color: var(--primary-red-color);
		font-size: 1.3rem;
	}

	nav ul li span:last-child {
		font-size: 1.8rem;
	}

	nav + span {
		font-size: 2.5rem;
		cursor: pointer;
	}

	span.diagonal-line {
		margin-inline: 0.5rem;
		position: relative;
		top: 2rem;
		left: 0.8rem;
		width: 3.5rem;
		border-bottom-width: 0.3rem;
	}

	.sidebar {
		display: flex;
		flex-direction: column;
		align-self: flex-start;
		gap: 1rem;
	}

	.sidebar > :first-child {
		color: var(--primary-red-color);
		font-size: 1.4rem;
		text-transform: uppercase;
	}

	.sidebar > :last-child {
		display: flex;
		gap: 3rem;
	}

	.sidebar > :last-child > div {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
		cursor: pointer;
	}

	.sidebar > :last-child > div > :first-child {
		font-size: 1.6rem;
	}

	.sidebar > :last-child > div > :last-child {
		font-size: 1.1rem;
		font-style: italic;
	}
</style>
