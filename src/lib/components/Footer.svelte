<script lang="ts">
	import Logo from "$lib/components/Icons/Logo.svelte"

	const navItems = ["EV news", "EV ревюта", "EV masters", "календар", "публикации"];
	const menu = ["За нас", "Партньори", "Контакти", "Общи условия", "Новини за EV News", "Tвоята EV Kола"];
</script>

<footer class="wrapper">
	<div class="logo-container">
		<Logo />

		<div class="stripes" />
	</div>

	<div class="content">
		<div>
			<nav class="primary-nav">
				<ul>
					{#each navItems as item, i}
						<li class:text-gray={i === 3 || i === 4}>
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
			<div class="icon">✉️</div>

			<div class="email-container">
				<div class="text">Контакти</div>
				<div class="email">info@carlifebydani.com</div>
				<div class="description">Имате нужда от повече информация или връзка с нас.</div>
			</div>

			<div class="anchor" />
		</div>
	</div>

	<div class="rights">&copy; 2023 carlifebydani.com. Всички права запазени!</div>
</footer>

<style>
	footer {
		padding-block: 5rem;
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
		max-width: 17rem;
		height: fit-content;
	}

	.logo-container .stripes {
		flex: 1;
		height: 100%;
		background: var(--stripes-bg-3);
	}

	.content {
		display: flex;
		justify-content: space-between;
	}

	.primary-nav ul {
		margin-bottom: 4rem;
		display: flex;
		gap: 3rem;
		text-transform: capitalize;
		font-size: 1.8rem;
	}

	.secondary-nav ul {
		display: flex;
		flex-wrap: wrap;
		gap: 1.5rem;
		width: 50%;
		font-size: 1.2rem;
	}

	.primary-nav ul li,
	.secondary-nav ul li {
		cursor: pointer;
	}

	.contact {
		display: flex;
		gap: 1rem;
	}

	.contact .icon {
		align-self: center;
		font-size: 7rem;
	}

	.contact .email-container .text {
		margin-bottom: 1.5rem;
		color: var(--primary-red-color);
		font-size: 1.2rem;
	}

	.contact .email-container .email {
		margin-bottom: 1rem;
		font-size: 2.5rem;
	}

	.contact .email-container .description {
		font-size: 1rem;
		color: var(--font-color-gray);
	}

	.contact .anchor {
		margin-left: 4rem;
		position: relative;
		width: 10rem;
		height: 10rem;
		border-radius: 50%;
		background-color: var(--primary-red-color);
		cursor: pointer;
	}

	.contact .anchor::after {
		content: "";
		position: absolute;
		top: 40%;
		left: 40%;
		width: 2rem;
		height: 2rem;
		border-top: 0.5rem solid var(--font-color-white);
		border-left: 0.5rem solid var(--font-color-white);
		rotate: 45deg;
	}

	.rights {
		margin-top: 5rem;
		padding-top: 5rem;
		border-top: 0.2rem solid var(--delimiter);
		text-align: center;
		font-size: 1.3rem;
	}
</style>
