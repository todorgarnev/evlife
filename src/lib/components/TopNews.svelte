<section class="wrapper">
	<div class="top-to-bottom-overlay" />

	<div class="image-container">
		<div />
	</div>

	<div class="info-container">
		<div>
			<span>EV ревюта</span>
			&#x2022;
			<span>04.10.2023</span>
		</div>

		<div>VW ID. BUZZ <br /> Няма как да не го харесате, страхотен е!</div>
	</div>
</section>

<style>
	section {
		position: relative;
		padding-block: 3rem 7rem;
		background: var(--secondary-bg-color);
		color: var(--font-color-white);
	}

	.image-container {
		position: inherit;
		width: 96rem;
		height: 54rem;
		border-bottom-right-radius: 10rem;
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
		border-bottom-right-radius: 13rem;
	}

	.image-container > div {
		width: 100%;
		height: 100%;
		background: var(--bottom-to-top-overlay);
		border-bottom-right-radius: 10rem;
	}

	.info-container {
		padding: 4rem;
		position: absolute;
		top: 5rem;
		right: calc((100vw - var(--max-width)) / 2);
		width: 50rem;
		height: 34rem;
		border-bottom-right-radius: 5rem;
		background-color: var(--primary-red-color);
		z-index: 1;
	}

	.info-container > div:first-child {
		margin-bottom: 3rem;
		color: var(--font-color-black);
	}

	.info-container > div:first-child > :first-child {
		font-size: 2rem;
		font-weight: bold;
		text-transform: uppercase;
	}

	.info-container > div:first-child > :last-child {
		font-size: 1.6rem;
	}

	.info-container > div:last-child {
		font-size: 4rem;
	}
</style>
