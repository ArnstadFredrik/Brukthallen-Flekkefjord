<script>
	let { title, children, fullwidth = false } = $props();
</script>

<section class={fullwidth ? 'fullwidth' : 'content'}>
	{#if title}
		<h2>{title}</h2>
	{/if}

	{@render children()}
</section>
