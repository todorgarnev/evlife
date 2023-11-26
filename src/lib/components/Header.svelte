<script lang="ts">
	import Logo from "$lib/assets/images/logo.png";

	const navItems = ["EV news", "EV ревюта", "EV masters"];
	const navItemsSoon = ["календар", "публикации"];
</script>

<header class="wrapper">
	<img class="logo" src={Logo} alt="Carlife by Dani Logo" />

	<nav>
		<ul>
			{#each navItems as item, i}
				<li>
					<span class="sub-title">{String(i + 1).padStart(2, "0")}</span>
					<span class="title">{item}</span>
				</li>
			{/each}

			{#each navItemsSoon as item}
				<li>
					<span class="sub-title">Скоро</span>
					<span class="title soon text-gray">{item}</span>
				</li>
			{/each}
		</ul>
	</nav>

	<span class="magnifier">🔍</span>

	<span class="diagonal-line" />

	<div class="sidebar">
		<span class="sidebar-title">сподели с нас...</span>

		<div class="sidebar-items">
			<div class="sidebar-item">
				<span class="item-title">Новини за EV NEWS</span>
				<span class="item-sub-title text-gray">Теми, които те вълнуват</span>
			</div>

			<div class="sidebar-item">
				<span class="item-title">Твоята EV Кола</span>
				<span class="item-sub-title text-gray">Запиши колата си за ревю</span>
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

	.logo {
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

	.sub-title {
		color: var(--primary-red-color);
		font-size: 1.3rem;
	}

	.title {
		font-size: 1.8rem;
	}

	.magnifier {
		font-size: 2.5rem;
		cursor: pointer;
	}

	.diagonal-line {
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

	.sidebar-title {
		color: var(--primary-red-color);
		font-size: 1.3rem;
		text-transform: uppercase;
	}

	.sidebar-items {
		display: flex;
		gap: 3rem;
	}

	.sidebar-item {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
		cursor: pointer;
	}

	.item-title {
		font-size: 1.6rem;
	}

	.item-sub-title {
		font-size: 1.1rem;
		font-style: italic;
	}
</style>
