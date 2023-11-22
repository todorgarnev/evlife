<script lang="ts">
	import "./styles.css";

	const topics = ["tesla", "EVРевюта", "EVMasters", "батерии", "зареждане", "cyberTruck"];
	const menu = ["за нас", "партньори", "контакти", "общи условия"];
</script>

<section class="wrapper">
	<span>популярни теми</span>

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

	<button class="button">💖 подкрепи ни</button>
</section>
