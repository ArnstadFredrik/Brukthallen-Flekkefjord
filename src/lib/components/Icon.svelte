<script>
	let { color = 'white', mdi, size = 1, fill } = $props();
	const htmlSize = `${size * 1.5}rem`;

	if (fill) color = undefined;
</script>

<svg viewBox="0 0 24 24" width={htmlSize} height={htmlSize}>
	<path fill={color} d={mdi} style="fill: var({fill});" />
</svg>
