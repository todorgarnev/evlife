<section class="wrapper">
	<div>
		<div>сподели с нас</div>

		<div class="text-gray">
			Lorem ipsum е елементарен примерен текст, използван в печатарската и типографската индустрия.
		</div>
	</div>

	<div />

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
		grid-template-columns: 31.5rem 7rem 5.5rem 40rem 3rem 40rem;
		grid-template-rows: 60rem;
		background-color: var(--primary-bg-color);
		color: var(--font-color-white);
	}

	section > :first-child {
		padding-top: 5rem;
		grid-column: 1/2;
	}

	section > :first-child > :first-child {
		margin-bottom: 4.5rem;
		padding-block: 1.5rem;
		padding-left: 2rem;
		border-left: 1rem solid var(--primary-red-color);
		font-size: 3.5rem;
		text-transform: uppercase;
	}

	section > :first-child > :last-child {
		font-size: 1.3rem;
		line-height: 1.5;
	}

	section > :nth-child(2) {
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
		font-size: 2.5rem;
	}

	.card-description {
		position: inherit;
		font-size: 1.6rem;
		font-style: italic;
	}
</style>
