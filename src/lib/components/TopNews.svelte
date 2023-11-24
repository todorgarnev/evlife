<section class="wrapper">
	<div class="top-to-bottom-overlay" />

	<div class="image-container">
		<div />
	</div>

	<div class="info-container">
		<div class="title">
			<span>EV ревюта</span>
			&#x2022;
			<span>04.10.2023</span>
		</div>

		<div class="description">VW ID. BUZZ <br /> Няма как да не го харесате, страхотен е!</div>
	</div>
</section>

<style>
	section {
		position: relative;
		padding-block: 3rem 7rem;
		background: var(--stripes-bg-1);
		color: var(--font-color-white);
	}

	.image-container {
		position: inherit;
		width: 96rem;
		height: 54rem;
		border-bottom-right-radius: var(--border-bottom-right-radius-3);
		background-color: dodgerblue;
		z-index: 1;
	}

	.image-container::after {
		content: "";
		position: absolute;
		top: 0;
		bottom: -4rem;
		left: 0;
		right: -4rem;
		border-bottom: 2rem solid var(--primary-gray-color);
		border-right: 2rem solid var(--primary-gray-color);
		border-bottom-right-radius: var(--border-bottom-right-radius-4);
	}

	.image-container > div {
		width: 100%;
		height: 100%;
		background: var(--bottom-to-top-overlay);
		border-bottom-right-radius: var(--border-bottom-right-radius-3);
	}

	.info-container {
		padding: 4rem;
		position: absolute;
		top: 5rem;
		right: calc((100vw - var(--max-width)) / 2);
		width: 50rem;
		height: 34rem;
		border-bottom-right-radius: var(--border-bottom-right-radius-2);
		background-color: var(--primary-red-color);
		z-index: 1;
	}

	.title {
		margin-bottom: 3rem;
		color: var(--font-color-black);
	}

	.title > :first-child {
		font-size: 2rem;
		font-weight: bold;
		text-transform: uppercase;
	}

	.title > :last-child {
		font-size: 1.6rem;
	}

	.description {
		font-size: 4rem;
	}
</style>
