<script lang="ts">
	const topics = ["tesla", "EVРевюта", "EVMasters", "батерии", "зареждане", "cyberTruck"];
	const menu = ["за нас", "партньори", "контакти", "общи условия"];
</script>

<section class="wrapper">
	<span class="text-uppercase">популярни теми</span>

	<span class="diagonal-line" />

	<nav>
		<ul>
			{#each topics as topic}
				<li>#{topic}</li>
			{/each}
		</ul>
	</nav>

	<nav>
		<ul>
			{#each menu as item}
				<li>{item}</li>
			{/each}
		</ul>
	</nav>

	<button>💖 подкрепи ни</button>
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

	span.diagonal-line {
		margin-inline: 0.5rem;
		position: relative;
		top: 1.5rem;
		left: 1rem;
	}

	nav ul {
		display: flex;
		gap: 1.5rem;
		text-transform: capitalize;
	}

	nav ul li {
		cursor: pointer;
	}

	nav:first-of-type {
		margin-right: auto;
		font-size: 1.2rem;
	}

	button {
		margin-left: 2rem;
		padding: 1rem 1.5rem;
		width: max-content;
		background-color: var(--button-bg);
		color: var(--font-color-white);
		font-size: 1.4rem;
		font-weight: bold;
		text-transform: uppercase;
		cursor: pointer;
	}
</style>
