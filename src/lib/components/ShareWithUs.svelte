<section class="wrapper">
	<div class="share-with-us">
		<div class="title bordered-title">сподели с нас</div>

		<div class="description text-gray">
			Lorem Ipsum е елементарен примерен текст, използван в печатарската и типографската индустрия.
		</div>
	</div>

	<div class="stripes" />

	<div class="card">
		<div class="card-overlay" />

		<div class="card-title">Новини за EV News</div>

		<div class="card-description text-gray">Теми, които ме вълнуват</div>
	</div>

	<div class="card">
		<div class="card-overlay" />

		<div class="card-title">Твоята EV Кола</div>

		<div class="card-description text-gray">Запиши колата си за ревю</div>
	</div>
</section>

<style>
	section {
		padding-block: 8.5rem 7.5rem;
		display: grid;
		grid-template-columns: 32rem auto 5.5rem 41.2rem 3.2rem 41.2rem;
		grid-template-rows: 60rem;
		background-color: var(--primary-bg-color);
	}

	.share-with-us {
		padding-top: 5rem;
		grid-column: 1/2;
	}

	.share-with-us .title {
		margin-bottom: 4rem;
	}

	.share-with-us .description {
		font-size: 1.5rem;
		line-height: 2.2rem;
	}

	.stripes {
		margin-block: 5rem;
		grid-column: 3/4;
		background:
			url(../assets/stripes-bg-3.png),
			lightgray 0% 0% / 5rem 5rem repeat;
		background-color: var(--primary-bg-color);
	}

	section > :nth-child(3) {
		grid-column: 4/5;
		background:
			url("../assets/share-with-us-1.png"),
			lightgray 50% / cover no-repeat;
	}

	section > :last-child {
		grid-column: 6/7;

		background:
			url("../assets/share-with-us-2.png"),
			lightgray 50% / cover no-repeat;
	}

	.card {
		padding: 5.5rem 8.5rem;
		position: relative;
		text-align: center;
		border-bottom-right-radius: var(--border-bottom-right-radius-2);
		cursor: pointer;
	}

	.card:hover .card-overlay {
		background: linear-gradient(180deg, var(--primary-red-color) 0%, rgba(254, 54, 82, 0) 100%);
	}

	.card:hover .card-description {
		color: var(--font-color-black);
	}

	.card-overlay {
		position: absolute;
		inset: 0;
		background: linear-gradient(180deg, rgba(27, 27, 27, 0.9) 0%, rgba(27, 27, 27, 0) 100%);
	}

	.card-title {
		margin-bottom: 1rem;
		position: inherit;
		color: var(--font-color-white);
		font-size: 2.8rem;
		font-weight: 700;
	}

	.card-description {
		position: inherit;
		font-size: 1.7rem;
		font-style: italic;
	}
</style>
