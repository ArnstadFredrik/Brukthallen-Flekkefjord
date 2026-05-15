<script>
	import hero from '$lib/assets/brukthallen_web.webp?enhanced';
</script>

<header class="hero-section fullwidth">
	<enhanced:img class="hero-img" src={hero} alt="Fasaden av Brukthallen i Flekkefjord" />
	<h1 class="hero-title">Brukthallen<br />Flekkefjord</h1>
</header>

<style lang="postcss">
	@reference "tailwindcss";

	.hero-section {
		display: grid;
		grid-template-columns: subgrid;
		grid-template-rows: 1fr 10rem;
		overflow: hidden;
		place-content: center;
	}

	.hero-img,
	picture {
		grid-column: full;
		max-height: calc(100svh - 10rem);
		object-fit: cover;
	}

	/*.hero-img,
	picture,
	.hero-title {
		grid-row: 1/-1;
	}*/

	.hero-title {
		grid-column: full;
		width: 100%;
		padding: 2rem;
		place-self: center;
		background-color: lab(from var(--bg) l a b / 75%);
		grid-row: initial;

		@media (max-width: 425px) {
			grid-row: initial;
		}
	}
</style>
