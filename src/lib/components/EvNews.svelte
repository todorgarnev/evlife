<script lang="ts">
	import BigEvNewsImg1 from "../assets/big-ev-news-1.png";
	import BigEvNewsImg2 from "../assets/big-ev-news-2.png";
	import BigEvNewsImg3 from "../assets/big-ev-news-3.png";
	import SmallEvNewsImg1 from "../assets/small-ev-news-1.png";
	import SmallEvNewsImg2 from "../assets/small-ev-news-2.png";
	import SmallEvNewsImg3 from "../assets/small-ev-news-3.png";
	import SmallEvNewsImg4 from "../assets/small-ev-news-4.png";

	const primaryNews = [
		{
			date: "04.09.2023",
			description: "Tesla API, Пожар на Лутън, Mercedes eActros 600"
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
			description: "TESLA M3 Highland, Cybertruck, CATL"
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

	const getBigImg = (i: number) => {
		switch (i) {
			case 1:
				return BigEvNewsImg1;
			case 2:
				return BigEvNewsImg2;
			case 3:
				return BigEvNewsImg3;
			default:
				break;
		}
	};

	const getSmallImg = (i: number) => {
		switch (i) {
			case 1:
				return SmallEvNewsImg1;
			case 2:
				return SmallEvNewsImg2;
			case 3:
				return SmallEvNewsImg3;
			case 4:
				return SmallEvNewsImg4;
			default:
				break;
		}
	};
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">ev news</div>

		<button class="button">виж всички</button>
	</header>

	<div class="primary-items">
		{#each primaryNews as item, i}
			<div class="news-card big-news-card">
				<div class="card-image">
					<div class="overlay" />

					<img src={getBigImg(i + 1)} alt="Big News" />

					<div class="title">{item.date}</div>
				</div>

				<div class="description">{item.description}</div>
			</div>
		{/each}
	</div>

	<div class="secondary-items">
		{#each secondaryNews as item, i}
			<div class="news-card small-news-card">
				<div class="card-image">
					<div class="overlay" />

					<img src={getSmallImg(i + 1)} alt="Small News" />

					<div class="title">{item.date}</div>
				</div>

				<div class="description">{item.description}</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 4rem 4.4rem;
		background: var(--stripes-bg-2);
	}

	.primary-items {
		margin-bottom: 3.2rem;
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 3.2rem;
	}

	.secondary-items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3.2rem;
	}
</style>
