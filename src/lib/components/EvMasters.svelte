<script lang="ts">
	import MasterImg1 from "../assets/masters-1.png";
	import MasterImg2 from "../assets/masters-2.png";
	import MasterImg3 from "../assets/masters-3.png";
	import MasterImg4 from "../assets/masters-4.png";

	const masters = [
		{
			date: "04.09.2023",
			description: "Станислав Михов (SENTO) - Защо избра TESLA?"
		},
		{
			date: "04.09.2023",
			description: 'Volvo C40 Recharge - "Светлин Стайков - приключения с електромобили'
		},
		{
			date: "04.09.2023",
			description: 'Виктор Стоянов - Как реших да карам електромобил?'
		},
		{
			date: "04.09.2023",
			description: "Мъри Иванов - Fines charging и електромобилите"
		}
	];

	const getImg = (i: number) => {
		switch (i) {
			case 1:
				return MasterImg1;
			case 2:
				return MasterImg2;
			case 3:
				return MasterImg3;
			case 4:
				return MasterImg4;
			default:
				break;
		}
	};
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">ev masters</div>

		<button class="button">виж всички</button>
	</header>

	<div class="items">
		{#each masters as item, i}
			<div class="news-card small-news-card">
				<div class="card-image">
					<div class="overlay" />

					<img src={getImg(i + 1)} alt="Big News" />

					<div class="title">{item.date}</div>
				</div>

				<div class="description">{item.description}</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 4rem 4.6rem;
		background:
			url("../assets/stripes-bg-2.png"),
			lightgray 0% 0% / 5rem 5rem repeat;
			background-color: var(--secondary-bg-color);
	}

	.items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3.2rem;
	}
</style>
