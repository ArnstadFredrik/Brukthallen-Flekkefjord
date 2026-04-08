<script>
	import hero from '$lib/assets/store-front.jpg?enhanced';
	import Contact from '$lib/components/Contact.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import GoogleMap from '$lib/components/GoogleMap.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Icon from '$lib/components/Icon.svelte';
	import { mdiMapMarker, mdiPhone } from '@mdi/js';
</script>

<svelte:head>
	<title>Brukthallen Flekkefjord</title>
</svelte:head>

<Hero />

<!-- <section>
	<h2>Om Oss</h2>
	<p>
		Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iste minima delectus dignissimos in
		temporibus fuga esse quam natus, sapiente obcaecati vitae, officia ea adipisci assumenda
		repudiandae quo? Beatae, aspernatur! Voluptas ad vel provident quibusdam aliquid deleniti natus
		fugiat vitae, facere magni repellat, sequi placeat officia autem perspiciatis, ducimus
		voluptatibus expedita facilis aliquam eligendi? Commodi iste ex maiores repudiandae molestias.
		Aliquam quibusdam magnam optio ad assumenda voluptatum corrupti repellendus ipsum quis
		accusantium accusamus rem id, sed illum incidunt minima cumque quos repellat iusto consequatur
		molestiae ullam eligendi aperiam. Tenetur assumenda optio at consectetur quam, soluta numquam,
		reiciendis impedit, quibusdam ullam possimus.
	</p>
</section>
 -->
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
	<Contact />

	<div class="icon-line grid">
		<Icon mdi={mdiMapMarker} size="1" fill="--color-emerald-900" />
		<a
			href="https://www.google.com/maps/place/Brukthallen+Flekkefjord/@58.294074,6.667087,1048m/data=!3m1!1e3!4m6!3m5!1s0x4639dd004eb68961:0xf638d641d4e35110!8m2!3d58.2940737!4d6.6670868!16s%2Fg%2F11x0dr51j9?hl=no&entry=ttu&g_ep=EgoyMDI2MDQwNS4wIKXMDSoASAFQAw%3D%3D"
			target="_blank"
		>
			Jernbaneveien 10, 4405 Flekkefjord
		</a>
	</div>

	<GoogleMap width="100%" />
</section>

<style lang="postcss">
	@reference "tailwindcss";

	section {
		grid-column: content;
		display: grid;
		grid-template-columns: subgrid;
		gap: 0.8rem;
		background-color: var(--bg);
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

	table,
	tbody,
	tr,
	td {
		display: grid;
	}
	thead {
		display: none;
	}

	tr:nth-of-type(1n) {
		background-color: var(--color-emerald-100);
	}
	tr:nth-of-type(2n) {
		background-color: var(--color-emerald-50);
	}

	tbody tr {
		grid-template-columns: 1fr 1fr;
		gap: 0.5rem;
		padding: 0.5rem;
	}
</style>
