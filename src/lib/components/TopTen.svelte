<script lang="ts">
	import CarLife from "$lib/components/Icons/CarLife.svelte";

	const topTen = [
		{
			title: "ev ревюта",
			description: "VW ID4 GTX - Изненадващо добър и много стилен"
		},
		{
			title: "ev ревюта",
			description: 'Volvo C40 Recharge - "Първият" електромобил на Volvo'
		},
		{
			title: "ev ревюта",
			description: 'Nissan Ariya - "Nissan - Megane " скъпият японски SUV'
		},
		{
			title: "ev ревюта",
			description: "Citroen AMI - Движи се, но електромобил ли е?"
		},
		{
			title: "ev masters",
			description: "Виктор Стоянов - Как реших да карам електромобил?"
		},
		{
			title: "ev ревюта",
			description: "BMW iX M60 - Кралят на SUV-овете (EV)"
		},
		{
			title: "ev news",
			description: "Cybertruck, Porsche Macan EV, MG не може да бъде спрян"
		},
		{
			title: "ev news",
			description: "Tesla M3 Highland, Cybertruck, CATL"
		},
		{
			title: "ev news",
			description: "Tesla новини, NACS + VW, Model S Plaid и сцеплението"
		},
		{
			title: "ev ревюта",
			description: "Megane E-Tech - Удобен за града и около него"
		}
	];
</script>

<section class="wrapper">
	<header>
		<div class="header-title bordered-title">
			<CarLife />
			top 10
		</div>

		<div class="header-description text-gray">
			Car Life top 10 е седмична класация. <br /> Период на класацията 16.11 - 22.11.2023
		</div>
	</header>

	<div class="cards">
		{#each topTen as item, i}
			<div class="card">
				<div class="number">{String(i + 1).padStart(2, "0")}</div>

				<div class="text">
					<div class="title">{item.title}</div>
					<div class="description">{item.description}</div>
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 5rem;
		background-color: var(--secondary-bg-color);
	}

	header {
		margin-bottom: 4rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.header-title {
		display: flex;
		align-items: center;
		gap: 1.7rem;
	}

	.header-description {
		/* text-align: right; */
		font-size: 1.2rem;
		line-height: 1.6rem;
	}

	.cards {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: repeat(5, 1fr);
		grid-auto-flow: column;
		gap: 1rem;
	}

	.card {
		padding: 1.3rem 3.8rem 0.7rem 2.2rem;
		display: flex;
		gap: 3.5rem;
		background-color: var(--primary-bg-color);
		border-bottom-right-radius: var(--border-bottom-right-radius-1);
	}

	.card .text {
		padding-top: 1rem;
	}

	.card .number {
		color: var(--secondary-bg-color);
		font-size: 10rem;
		font-weight: 700;
		line-height: 10rem;
	}

	.text .title {
		margin-bottom: 0.75rem;
		color: var(--primary-red-color);
		font-size: 1.3rem;
		text-transform: uppercase;
	}

	.text .description {
		color: var(--font-color-white);
		font-size: 2rem;
		font-weight: 700;
		line-height: 2.6rem;
	}
</style>
