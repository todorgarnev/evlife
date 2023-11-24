<script lang="ts">
	const primaryNews = [
		{
			date: "04.09.2023",
			description: "Tesla API, Пожар на  Лутън, Mercedes eActros 600"
		},
		{
			date: "04.09.2023",
			description: "Cybertruck, Porsche Macan EV, MG не може да бъде спрян"
		},
		{
			date: "04.09.2023",
			description: "Tesla M3P Highland, Gigapress V2, Toyota отливки"
		}
	];
	const secondaryNews = [
		{
			date: "04.09.2023",
			description: "Tesla M3 Highland, Cybertruck, CATL"
		},
		{
			date: "04.09.2023",
			description: "VW, Toyota, Tesla и бъдещето"
		},
		{
			date: "04.09.2023",
			description: "Toyota новини, NACS + Mercedes"
		},
		{
			date: "04.09.2023",
			description: "Tesla новини, NACS + VW, Model S Plaid и сцеплението"
		}
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">ev news</div>

		<button class="button"> виж всички</button>
	</header>

	<div class="primary-items">
		{#each primaryNews as item}
			<div class="big-news-card">
				<div class="card-image">
					<div />
				</div>

				<div class="content">
					<div class="title">{item.date}</div>
					<div class="description">{item.description}</div>
				</div>
			</div>
		{/each}
	</div>

	<div class="secondary-items">
		{#each secondaryNews as item}
			<div class="small-news-card">
				<div class="card-image">
					<div />
				</div>

				<div class="content">
					<div class="title">{item.date}</div>
					<div class="description">{item.description}</div>
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 4rem;
		background: var(--secondary-bg-stripes);
	}

	.primary-items {
		margin-bottom: 3rem;
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 3rem;
	}

	.secondary-items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3rem;
	}
</style>
