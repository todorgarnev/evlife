<script lang="ts">
	import imageSrc from "$lib/assets/VW_ID_Buzz.png";
	import CurvedLine from "./Icons/CurvedLine.svelte";
	import Dot from "./Icons/Dot.svelte";
</script>

<section class="wrapper">
	<div class="top-to-bottom-overlay" />

	<div class="image-container">
		<img src={imageSrc} alt="Top news" />

		<span class="curved-line">
			<CurvedLine />
		</span>

		<div />
	</div>

	<div class="info-container">
		<div class="title">
			<span>EV ревюта</span>
			<Dot />
			<span>04.10.2023</span>
		</div>

		<div class="description">VW ID. BUZZ <br /> Няма как да не го харесате, страхотен е!</div>
	</div>
</section>

<style>
	section {
		position: relative;
		padding-block: 3rem 7rem;
		background:
			url("../assets/stripes-bg-1.png"),
			lightgray 0% 0% / 5rem 5rem repeat;
		background-color: var(--secondary-bg-color);
	}

	.image-container {
		position: inherit;
		width: 100%;
		max-width: 96rem;
		height: 100%;
		max-height: 54rem;
		border-bottom-right-radius: var(--border-bottom-right-radius-3);
		z-index: 1;
	}

	.curved-line {
		position: absolute;
		top: 0;
		right: -4rem;
	}

	.image-container > div {
		position: absolute;
		inset: 0;
		background: var(--bottom-to-top-overlay);
		border-bottom-right-radius: var(--border-bottom-right-radius-3);
		opacity: 0.6;
	}

	.image-container > img {
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
		cursor: pointer;
		z-index: 1;
	}

	.info-container:hover .description {
		color: var(--font-color-black);
		transition: all 0.3s;
	}

	.title {
		margin-bottom: 2rem;
		display: flex;
		align-items: center;
		color: var(--font-color-black);
	}

	.title > :first-child {
		margin-right: 1rem;
		font-size: 2rem;
		font-weight: 700;
		text-transform: uppercase;
	}

	.title > :last-child {
		margin-left: 1rem;
		font-size: 1.7rem;
	}

	.description {
		color: var(--font-color-white);
		font-size: 4.6rem;
		font-weight: 700;
		line-height: 4.4rem;
	}
</style>
