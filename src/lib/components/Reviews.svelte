<script lang="ts">
	const reviews = [
		{
			date: "04.09.2023",
			description: "VW ID4 GTX - Изненадващо добър и много стилен"
		},
		{
			date: "04.09.2023",
			description: 'Volvo C40 Recharge - "Първият" електромобил на Volvo'
		},
		{
			date: "04.09.2023",
			description: 'Nissan Ariya - "Nissan - Megane " скъпият японски SUV'
		},
		{
			date: "04.09.2023",
			description: "Citroen AMI - Движи се, но електромобил ли е?"
		},
		{
			title: "ev masters",
			description: "Виктор Стоянов - Как реших да карам електромобил?"
		},
		{
			date: "04.09.2023",
			description: "BMW iX M60 - Кралят на SUV-овете (EV)"
		},
		{
			date: "04.09.2023",
			description: "Cybertruck, Porsche Macan EV, MG не може да бъде спрян"
		},
		{
			date: "04.09.2023",
			description: "Tesla M3 Highland, Cybertruck, CATL"
		}
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">ev ревюта</div>

		<button class="button">виж всички</button>
	</header>

	<div class="items">
		{#each reviews as item}
			<div class="news-card small-news-card">
				<div class="card-image">
					<div class="overlay" />

					<div class="title">{item.date}</div>
				</div>

				<div class="description">{item.description}</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 4rem;
		background: var(--secondary-bg-color);
	}

	.items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3rem;
	}
</style>
