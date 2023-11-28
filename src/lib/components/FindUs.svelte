<script lang="ts">
	import Youtube from "$lib/components/Icons/Youtube.svelte";
	import Patreon from "./Icons/Patreon.svelte";
	import Facebook from "./Icons/Facebook.svelte";
	import Instagram from "./Icons/Instagram.svelte";
	import TikTok from "./Icons/TikTok.svelte";
	import Spotify from "./Icons/Spotify.svelte";
	import Podcast from "./Icons/Podcast.svelte";

	const socials = [
		{
			icon: Youtube,
			title: "@CarlifebyDani"
		},
		{
			icon: Patreon,
			title: "@carlifebydani"
		},
		{
			icon: Facebook,
			title: "@carlifebydani"
		},
		{
			icon: Instagram,
			title: "@carlifebydani"
		},
		{
			icon: TikTok,
			title: "@carlifebydani"
		},
		{
			icon: Spotify,
			title: "@CarlifebyDani"
		},
		{
			icon: Podcast,
			title: "@CarlifebyDani"
		}
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">намерете ни в</div>
	</header>

	<div class="cards">
		{#each socials as item}
			<div class="card">
				<svelte:component this={item.icon} />

				<div class="title text-gray">{item.title}</div>
			</div>
		{/each}
	</div>
</section>

<style>
	section {
		padding-block: 5rem;
		background: var(--secondary-bg-color);
	}

	.cards {
		display: grid;
		grid-template-columns: repeat(7, 1fr);
		gap: 3rem;
	}

	.card {
		padding: 3.5rem 2.5rem 3rem 2.5rem;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		gap: 1.5rem;
		background-color: var(--primary-bg-color);
		border-bottom-right-radius: var(--border-bottom-right-radius-1);
	}

	.card .title {
		font-size: 1.2rem;
		font-weight: 700;
		line-height: 3.6rem;
	}
</style>
