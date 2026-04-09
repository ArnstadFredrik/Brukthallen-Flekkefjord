<script>
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<meta
		name="description"
		content="Bruktbutikken Brukthallen i Flekkefjord er en butikk som mottar og selger gjenbruksvarer i og rundt Flekkefjord."
	/>
	<meta
		name="keywords"
		content="brukt, bruktbutikk, flekkefjord, gjenbruk, second hand, upcycle, gjenbrukt, thrift store"
	/>
	<link rel="canonical" href="https://brukthallen.no" />
</svelte:head>

<main>
	{@render children()}

	<Footer />
</main>

<style lang="postcss">
	@reference "tailwindcss";

	main {
		--gap: 0.5rem;
		display: grid;
		background-color: var(--bg);
		min-block-size: 100svh;
		row-gap: 1rem;
		grid-template-columns:
			[full-start] minmax(var(--gap), auto) [content-start] minmax(auto, 75ch) [content-end] minmax(
				var(--gap),
				auto
			)
			[full-end];
	}

	*:has[main] {
		grid-column: content;
	}
</style>
