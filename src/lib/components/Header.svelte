<script lang="ts">
	import Logo from "$lib/components/Icons/Logo.svelte";
	import Search from "$lib/components/Icons/Search.svelte";
	import DiagonalLine from "./Icons/DiagonalLine.svelte";

	const navItems = ["EV News", "EV Ревюта", "EV Masters", "Новини", "Галерия"];

	let fill = $state("var(--font-color-white)");
</script>

<header class="wrapper">
	<div class="logo">
		<Logo />
	</div>

	<nav>
		<ul>
			{#each navItems as item, i}
				<li>
					<span class="sub-title">{String(i + 1).padStart(2, "0")}</span>
					<span class="title">{item}</span>
				</li>
			{/each}
		</ul>
	</nav>

	<span
		class="search"
		on:mouseover={() => (fill = "var(--primary-red-color)")}
		on:mouseleave={() => (fill = "var(--font-color-white)")}
	>
		<Search {fill} />
	</span>

	<DiagonalLine width={18} height={36} />

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
		padding-block: 1.5rem;
		display: flex;
		align-items: center;
		background-color: var(--primary-bg-color);
		color: var(--font-color-white);
		border-top: 0.1rem solid rgba(var(--primary-red-color-rgb), 0.5);
	}

	.logo {
		margin-right: 2.6rem;
		width: 100%;
		max-width: 22.4rem;
		height: 100%;
	}

	nav {
		margin-right: auto;
	}

	nav ul {
		display: flex;
		gap: 3rem;
	}

	nav ul li {
		display: flex;
		flex-direction: column;
		cursor: default;
	}

	nav ul li:hover {
		color: var(--primary-red-color);
		cursor: pointer;
		transition: all 0.3s;
	}

	.sub-title {
		color: var(--primary-red-color);
		font-size: 1.3rem;
	}

	.title {
		font-size: 2rem;
		font-weight: 700;
	}

	.search {
		margin-right: 1.6rem;
		cursor: pointer;
	}

	.sidebar {
		margin-left: 1.6rem;
		display: flex;
		flex-direction: column;
		align-self: flex-start;
		gap: 0.6rem;
	}

	.sidebar-title {
		color: var(--primary-red-color);
		font-size: 1.3rem;
		font-weight: 700;
		text-transform: uppercase;
	}

	.sidebar-items {
		display: flex;
		gap: 3rem;
	}

	.sidebar-item {
		display: flex;
		flex-direction: column;
		gap: 0.4rem;
		cursor: pointer;
	}

	.item-title {
		font-size: 1.7rem;
		font-weight: 700;
	}

	.item-title:hover {
		color: var(--primary-red-color);
		cursor: pointer;
		transition: all 0.3s;
	}

	.item-sub-title {
		font-size: 1.2rem;
		font-style: italic;
	}
</style>
