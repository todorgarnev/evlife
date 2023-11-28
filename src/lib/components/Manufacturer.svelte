<script lang="ts">
	import Tesla from "$lib/components/Icons/Tesla.svelte";
	import BMW from "$lib/components/Icons/BMW.svelte";
	import Mercedes from "$lib/components/Icons/Mercedes.svelte";
	import VW from "$lib/components/Icons/VW.svelte";
	import Audi from "$lib/components/Icons/Audi.svelte";
	import Porsche from "$lib/components/Icons/Porsche.svelte";
	import Mini from "$lib/components/Icons/Mini.svelte";
	import Volvo from "$lib/components/Icons/Volvo.svelte";
	import Polestar from "$lib/components/Icons/Polestar.svelte";
	import Hyundai from "$lib/components/Icons/Hyundai.svelte";
	import Kia from "$lib/components/Icons/Kia.svelte";
	import Renault from "$lib/components/Icons/Renault.svelte";
	import Nissan from "$lib/components/Icons/Nissan.svelte";
	import Toyota from "$lib/components/Icons/Toyota.svelte";
	import Opel from "$lib/components/Icons/Opel.svelte";
	import Citroen from "$lib/components/Icons/Citroen.svelte";
	import Peugeot from "$lib/components/Icons/Peugeot.svelte";
	import Ford from "$lib/components/Icons/Ford.svelte";
	import Byd from "$lib/components/Icons/Byd.svelte";
	import Lucid from "$lib/components/Icons/Lucid.svelte";
	import Nio from "$lib/components/Icons/Nio.svelte";
	import SecondCurvedLine from "./Icons/SecondCurvedLine.svelte";

	const brands = [
		Tesla,
		BMW,
		Mercedes,
		VW,
		Audi,
		Porsche,
		Mini,
		Volvo,
		Polestar,
		Hyundai,
		Kia,
		Renault,
		Nissan,
		Toyota,
		Opel,
		Citroen,
		Peugeot,
		Ford,
		Byd,
		Lucid,
		Nio
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">производител</div>

		<button class="button">виж всички</button>
	</header>

	<div class="container">
		<div class="curved-line">
			<SecondCurvedLine />
		</div>

		<div class="items">
			{#each brands as brand}
				<div class="brand">
					<svelte:component this={brand} />
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		padding-block: 5rem 4rem;
		background-color: var(--secondary-bg-color);
	}

	.container {
		position: relative;
	}

	.items {
		padding: 3rem 4rem 4.5rem 2.5rem;
		display: grid;
		grid-template-columns: repeat(7, 1fr);
		align-items: center;
		gap: 6rem;
		position: inherit;
		width: 100%;
		max-width: 126rem;
		background-color: var(--font-color-black);
		border-bottom-right-radius: var(--border-bottom-right-radius-3);
	}

	.brand {
		margin-inline: auto;
		cursor: pointer;
	}

	.curved-line {
		position: absolute;
		top: 0;
		right: -1.5rem;
	}
</style>
