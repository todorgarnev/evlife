<script lang="ts">
	const primaryNews = [
		{
			date: "04.09.2023",
			description: "Tesla с до $6300 отстъпки за нови автомобили"
		},
		{
			date: "04.09.2023",
			description: "Polestar 3 First Ride: Polestar's First SUV Has Great Expectations And A Big Price Tag"
		},
		{
			date: "04.09.2023",
			description: "Can Electric Bikes And Mopeds Reshape The Way People Move?"
		}
	];
	const secondaryNews = [
		{
			date: "04.09.2023",
			description: "What's The Real World Highway Range Of Today's Electric Cars? We Test To Find Out"
		},
		{
			date: "04.09.2023",
			description: "2024 Kia EV6: Price And EPA Range Overview"
		},
		{
			date: "04.09.2023",
			description: "Tesla's $2 Billion Investment In India Hinges On Import Tax Cuts For EVs: Report"
		},
		{
			date: "04.09.2023",
			description: "Non-Tesla EVs Can Now Supercharge In South Korea"
		},
		{
			date: "04.09.2023",
			description: "The Hyundai Ioniq 6 May Be The Most-Powerful N Car: Report"
		},
		{
			date: "04.09.2023",
			description: "Next-Gen Nissan Juke And Qashqai EVs To Be Made In The UK: Report"
		},
		{
			date: "04.09.2023",
			description: "The Lucid Air Sapphire Does 0 To 150 To 0 Four Seconds Quicker Than A 911 Turbo S"
		},
		{
			date: "04.09.2023",
			description: "EV Registrations In Europe Surpassed Diesel For The First Time"
		}
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">новини</div>

		<button class="button">виж всички</button>
	</header>

	<div class="primary-items">
		{#each primaryNews as item, i}
			<div class="news-card big-news-card">
				<div
					class="card-image"
					style="background: url('/src/lib/assets/big-news-{i + 1}.png'), lightgray 0% 0% / 5rem 5rem repeat;"
				>
					<div class="overlay" />

					<div class="title">{item.date}</div>
				</div>

				<div class="description">{item.description}</div>
			</div>
		{/each}
	</div>

	<div class="secondary-items">
		{#each secondaryNews as item, i}
			<div class="news-card small-news-card">
				<div
					class="card-image"
					style="background: url('/src/lib/assets/small-news-{i + 1}.png'), lightgray 0% 0% / 5rem 5rem repeat;"
				>
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
		padding-block: 4rem 6rem;
		background:
			url("../assets/stripes-bg-2.png"),
			lightgray 0% 0% / 50px 50px repeat;
		background-color: #202020;
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
