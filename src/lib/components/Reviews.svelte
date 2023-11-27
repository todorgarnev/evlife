<script lang="ts">
	import ReviewsImg1 from "../assets/review-1.png";
	import ReviewsImg2 from "../assets/review-2.png";
	import ReviewsImg3 from "../assets/review-3.png";
	import ReviewsImg4 from "../assets/review-4.png";
	import ReviewsImg5 from "../assets/review-5.png";
	import ReviewsImg6 from "../assets/review-6.png";
	import ReviewsImg7 from "../assets/review-7.png";
	import ReviewsImg8 from "../assets/review-8.png";

	const reviews = [
		{
			date: "04.09.2023",
			description: "Nissan Ariya - “Nissan - Megane” - скъпия японски SUV"
		},
		{
			date: "04.09.2023",
			description: "VW ID4 GTX - Изненадващо добър и много стилен"
		},
		{
			date: "04.09.2023",
			description: "Toyota bZ4X - Може да е скучна, но се справя в гората"
		},
		{
			date: "04.09.2023",
			description: "Volvo C40 Recharge - “Първият” електромобил на Volvo"
		},
		{
			title: "ev masters",
			description: "Citroen AMI - Движи се, но електромобил ли е?"
		},
		{
			date: "04.09.2023",
			description: "VW ID Buzz - Няма как да не го харесате, страхотен е!"
		},
		{
			date: "04.09.2023",
			description: "Volvo FX Electric Първият електрически камион в България"
		},
		{
			date: "04.09.2023",
			description: "BMW iX M60 - Кралят на SUV-овете (EV)"
		}
	];

	const getImg = (i: number) => {
		switch (i) {
			case 1:
				return ReviewsImg1;
			case 2:
				return ReviewsImg2;
			case 3:
				return ReviewsImg3;
			case 4:
				return ReviewsImg4;
			case 5:
				return ReviewsImg5;
			case 6:
				return ReviewsImg6;
			case 7:
				return ReviewsImg7;
			case 8:
				return ReviewsImg8;
			default:
				break;
		}
	};
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">ev ревюта</div>

		<button class="button">виж всички</button>
	</header>

	<div class="items">
		{#each reviews as item, i}
			<div class="news-card small-news-card">
				<div class="card-image">
					<div class="overlay" />

					<img src={getImg(i + 1)} alt="Review" />

					<div class="title">{item.date}</div>
				</div>

				<div class="description">{item.description}</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 5rem;
		background: var(--secondary-bg-color);
	}

	.items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3.2rem;
	}
</style>
