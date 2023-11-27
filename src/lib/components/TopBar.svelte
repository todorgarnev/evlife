<script lang="ts">
	import DiagonalLine from "./Icons/DiagonalLine.svelte";
	import Heart from "./Icons/Heart.svelte";

	const topics = ["Tesla", "EVРевюта", "EVMasters", "Батерии", "Зареждане", "CyberTruck"];
	const menu = ["За нас", "Партньори", "Контакти", "Общи условия"];
</script>

<section class="wrapper">
	<span class="text-uppercase text-bold">популярни теми</span>

	<DiagonalLine />

	<nav class="popular-topics">
		<ul>
			{#each topics as topic}
				<li>#{topic}</li>
			{/each}
		</ul>
	</nav>

	<nav class="menu">
		<ul>
			{#each menu as item}
				<li>{item}</li>
			{/each}
		</ul>
	</nav>

	<button class="button">
		<Heart />
		подкрепи ни
	</button>
</section>

<style>
	section {
		padding-block: 1rem;
		display: flex;
		align-items: center;
		background-color: var(--primary-bg-color);
		color: var(--font-color-white);
		font-size: 1.3rem;
	}

	span {
		margin-right: 1rem;
	}

	nav ul {
		display: flex;
		gap: 1.6rem;
	}

	nav ul li {
		cursor: pointer;
	}

	.popular-topics {
		margin-left: 1rem;
		margin-right: auto;
	}

	.menu {
		font-size: 1.4rem;
	}

	button {
		margin-left: 2rem;
		padding-inline: 1.2rem 1.8rem;
		display: flex;
		align-items: center;
		gap: 1rem;
	}
</style>
