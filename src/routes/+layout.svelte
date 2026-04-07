<script>
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<meta
		name="description"
		content="Bruktbutikken Brukthallen i Flekkefjord er en butikk som mottar og selger brukt varer i og rundt Flekkefjord."
	/>
	<meta name="keywords" content="brukt, bruktbutikk, flekkefjord, gjenbruk, second hand, upcycle" />
</svelte:head>

{@render children()}
