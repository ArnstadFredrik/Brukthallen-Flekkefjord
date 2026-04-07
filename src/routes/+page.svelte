<script>
	import hero from '$lib/assets/store-front.jpg?enhanced';
	import GoogleMap from '$lib/components/GoogleMap.svelte';
	import Icon from '$lib/components/Icon.svelte';
	import { mdiMapMarker, mdiPhone } from '@mdi/js';
</script>

<svelte:head>
	<title>Brukthallen Flekkefjord</title>
</svelte:head>

<main class="main">
	<header class="hero-section">
		<enhanced:img class="hero-img" src={hero} alt="" />
		<h1 class="hero-title">Brukthallen<br />Flekkefjord</h1>
	</header>

	<section>
		<h2>Om Oss</h2>
		<p>
			Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iste minima delectus dignissimos in
			temporibus fuga esse quam natus, sapiente obcaecati vitae, officia ea adipisci assumenda
			repudiandae quo? Beatae, aspernatur! Voluptas ad vel provident quibusdam aliquid deleniti
			natus fugiat vitae, facere magni repellat, sequi placeat officia autem perspiciatis, ducimus
			voluptatibus expedita facilis aliquam eligendi? Commodi iste ex maiores repudiandae molestias.
			Aliquam quibusdam magnam optio ad assumenda voluptatum corrupti repellendus ipsum quis
			accusantium accusamus rem id, sed illum incidunt minima cumque quos repellat iusto consequatur
			molestiae ullam eligendi aperiam. Tenetur assumenda optio at consectetur quam, soluta numquam,
			reiciendis impedit, quibusdam ullam possimus.
		</p>
	</section>

	<section>
		<h2>Åpningstider</h2>

		<table>
			<thead>
				<tr>
					<th heading="Dager">Dager</th>
					<th herading="Tid">Tid</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td heading="Dager">Onsdag og Fredag</td>
					<td heading="Tid">11:00-16:00</td>
				</tr>
				<tr>
					<td heading="Dager">Torsdag</td>
					<td heading="Tid">11:00-18:00</td>
				</tr>
				<tr>
					<td heading="Dager">Lørdag</td>
					<td heading="Tid">11:00-14:00</td>
				</tr>
			</tbody>
		</table>
	</section>

	<section>
		<h2>Kontakt oss</h2>

		<div class="icon-line grid">
			<Icon mdi={mdiPhone} size="1" fill="--color-emerald-900" />
			<p>900 71 827</p>
		</div>

		<div>
			<a href="/" class="button">Mail</a>
		</div>
		<div>
			<a href="https://www.facebook.com/profile.php?id=61571948758888" class="button">Facebook</a>
		</div>

		<h3>Kart</h3>

		<div class="icon-line grid">
			<Icon mdi={mdiMapMarker} size="1" fill="--color-emerald-900" />
			<p>Jernbaneveien 10, 4405 Flekkefjord</p>
		</div>

		<GoogleMap width="100%" />
	</section>

	<footer>
		<p>Brukthallen flekkefjord er drevet av frivillige for Flekkefjord Menighet</p>
	</footer>
</main>

<style lang="postcss">
	@reference "tailwindcss";

	.main {
		--gap: 0.1rem;
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

	section {
		grid-column: content;
		display: grid;
		gap: 0.5rem;
	}

	.hero-section {
		display: grid;
		grid-template-columns: subgrid;
		grid-column: full;
	}

	.hero-img,
	picture {
		grid-column: full;
	}

	.hero-img,
	picture,
	.hero-title {
		grid-row: 1/-1;
	}

	.hero-title {
		grid-column: full;
		width: 100%;
		padding: 2rem;
		place-self: center;
		background-color: lab(from var(--bg) l a b / 75%);

		@media (max-width: 425px) {
			grid-row: initial;
		}
	}

	table,
	tbody,
	tr,
	td {
		display: grid;
	}
	thead {
		display: none;
	}

	tbody tr {
		grid-template-columns: 1fr 1fr;
		gap: 0.5rem;
	}

	footer {
		grid-column: full;
		display: grid;
		grid-template-columns: subgrid;
		place-content: center;
		padding-block: 1rem;
		background-color: var(--base-clr);
		color: var(--color-emerald-100);

		p {
			grid-column: content;
		}
	}
</style>
