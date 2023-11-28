<script lang="ts">
	import Logo from "$lib/components/Icons/Logo.svelte";
	import Envelope from "$lib/components/Icons/Envelope.svelte";
	import Anchor from "$lib/components/Icons/Anchor.svelte";

	const navItems = ["EV News", "EV Ревюта", "EV Masters", "Новини", "Галерия"];
	const menu = ["За нас", "Партньори", "Контакти", "Общи условия", "Реклама", "Новини за EV News", "Твоята EV Кола"];
</script>

<footer class="wrapper">
	<div class="logo-container">
		<span class="logo">
			<Logo />
		</span>

		<div class="stripes" />
	</div>

	<div class="content">
		<div>
			<nav class="primary-nav">
				<ul>
					{#each navItems as item, i}
						<li>
							{item}
						</li>
					{/each}
				</ul>
			</nav>

			<nav class="secondary-nav">
				<ul>
					{#each menu as item}
						<li>
							{item}
						</li>
					{/each}
				</ul>
			</nav>
		</div>

		<div class="contact">
			<div class="envelope">
				<Envelope />
			</div>

			<div class="email-container">
				<div class="text">Контакти</div>
				<div class="email">info@carlifebydani.com</div>
				<div class="description">Имате нужда от повече информация или връзка с нас.</div>
			</div>

			<Anchor />
		</div>
	</div>

	<div class="rights">&copy; 2023 carlifebydani.com. Всички права запазени!</div>
</footer>

<style>
	footer {
		padding-block: 5rem 3rem;
		background-color: var(--primary-bg-color);
		color: var(--font-color-white);
	}

	.logo-container {
		margin-bottom: 5rem;
		display: flex;
		align-items: center;
		gap: 6rem;
		height: 10rem;
	}

	.logo-container .logo {
		width: 100%;
		max-width: 18.4rem;
		height: 100%;
	}

	.logo-container .stripes {
		flex: 1;
		height: 100%;
		background:
			url("../assets/stripes-bg-4.png"),
			lightgray 0% 0% / 5rem 5rem repeat;
		background-color: var(--font-color-black);
	}

	.content {
		display: flex;
		justify-content: space-between;
	}

	.primary-nav ul {
		margin-bottom: 3.2rem;
		display: flex;
		gap: 3rem;
		font-size: 2rem;
		font-weight: 700;
	}

	.secondary-nav ul {
		display: flex;
		flex-wrap: wrap;
		gap: 1.6rem;
		width: 70%;
		font-size: 1.4rem;
	}

	.primary-nav ul li,
	.secondary-nav ul li {
		cursor: pointer;
	}

	.contact {
		display: flex;
	}

	.envelope {
		align-self: center;
	}

	.email-container {
		margin-inline: 2.8rem 5.8rem;
	}

	.text {
		margin-bottom: 1.1rem;
		color: var(--primary-red-color);
		font-size: 1.3rem;
	}

	.email {
		margin-bottom: 0.4rem;
		font-size: 2.8rem;
		font-weight: 700;
	}

	.description {
		font-size: 1.2rem;
		color: var(--font-color-gray);
	}

	.rights {
		margin-top: 5rem;
		padding-top: 3.6rem;
		border-top: 0.2rem solid var(--delimiter);
		text-align: center;
		font-size: 1.4rem;
		font-weight: 700;
		line-height: 3.6rem;
	}
</style>
