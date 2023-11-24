<section class="wrapper">
	<div class="share-with-us">
		<div class="title bordered-title">сподели с нас</div>

		<div class="description text-gray">
			Lorem ipsum е елементарен примерен текст, използван в печатарската и типографската индустрия.
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
		padding-block: 7.5rem;
		display: grid;
		grid-template-columns: 31.5rem auto 5.5rem 40rem 3rem 40rem;
		grid-template-rows: 60rem;
		background-color: var(--primary-bg-color);
	}

	.share-with-us {
		padding-top: 5rem;
		grid-column: 1/2;
	}

	.share-with-us .title {
		margin-bottom: 4.5rem;
	}

	.share-with-us .description {
		font-size: 1.3rem;
		line-height: 1.5;
	}

	.stripes {
		margin-block: 5rem;
		grid-column: 3/4;
		background: var(--stripes-bg);
	}

	section > :nth-child(3) {
		grid-column: 4/5;
	}

	section > :last-child {
		grid-column: 6/7;
	}

	.card {
		padding: 6rem;
		position: relative;
		text-align: center;
		background-color: yellowgreen;
		border-bottom-right-radius: 5rem;
	}

	.card-overlay {
		position: absolute;
		inset: 0;
		background: var(--top-to-bottom-overlay);
	}

	.card-title {
		margin-bottom: 2rem;
		position: inherit;
		color: var(--font-color-white);
		font-size: 2.5rem;
	}

	.card-description {
		position: inherit;
		font-size: 1.6rem;
		font-style: italic;
	}
</style>
