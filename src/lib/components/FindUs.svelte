<script lang="ts">
	const socials = [
		{
			icon: "YouTube",
			title: "@CarlifebyDani"
		},
		{
			icon: "PATREON",
			title: "@carlifebyDani"
		},
		{
			icon: "FACEBOOK",
			title: "@carlifebyDani"
		},
		{
			icon: "INSTAGRAM",
			title: "@carlifebyDani"
		}
	];
</script>

<section class="wrapper">
	<header class="header">
		<div class="bordered-title">намерете ни в</div>
	</header>

	<div class="items">
		{#each socials as item}
			<div class="card">
				<div class="icon">{item.icon}</div>
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

	.items {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 3rem;
	}

	.card {
		padding: 8rem 4.5rem;
		background-color: var(--primary-bg-color);
		border-bottom-right-radius: 5rem;
		text-align: center;
	}

	.card .icon {
		margin-bottom: 3rem;
		color: var(--font-color-white);
		font-size: 4rem;
	}

	.card .title {
		font-size: 1.4rem;
	}
</style>
