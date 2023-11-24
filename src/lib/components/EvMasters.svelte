<script lang="ts">
	const masters = [
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
		}
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">ev masters</div>

		<button class="button">виж всички</button>
	</header>

	<div class="items">
		{#each masters as item}
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
		background: var(--stripes-bg-4);
	}

	.items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3rem;
	}
</style>
