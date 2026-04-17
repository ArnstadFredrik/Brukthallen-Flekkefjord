<script>
	import hero from '$lib/assets/store-front.jpg?enhanced';
	import Contact from '$lib/components/Contact.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import GoogleMap from '$lib/components/GoogleMap.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Icon from '$lib/components/Icon.svelte';
	import Section from '$lib/components/Section.svelte';
	import { mdiMapMarker, mdiPhone } from '@mdi/js';
</script>

<svelte:head>
	<title>Brukthallen Flekkefjord</title>
</svelte:head>

<Hero />

<Section title="Om Oss">
	<p>
		Brukthallen drives av Foreningen «Kirketorgets venner». Overskuddet går til det nye Kirketorget
		som skal bygges der Bondeheimen nå står. Brukthallen drives som et dugnadsprosjekt for
		realisering av et nytt flott bygg for hele kommunen der også Kirkekontorene vil inngå.
	</p>
</Section>

<Section title="Åpningstider">
	<table>
		<thead>
			<tr>
				<th heading="Dager">Dager</th>
				<th herading="Tid">Tid</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td heading="Dager">Mandal til Fredag</td>
				<td heading="Tid">11:00-16:00</td>
			</tr>
			<tr>
				<td heading="Dager">Lørdag</td>
				<td heading="Tid">11:00-15:00</td>
			</tr>
		</tbody>
	</table>
</Section>

<Section title="Levering og henting av varer">
	<p>
		Hele og rene varer tas hovedsakelig imot i butikkens åpningstider. Større gjenstander kan
		hentes. Dette gjøres i fortrinnsvis på onsdager eller etter avtale. Kontaktperson: Ivar Espenes,
		tlf: 902 08 024.
	</p>
	<p>
		Vi henter også varer i distriktene: Åna Sira, Feda, Gyland, Hidra og Sira, da etter faste
		tidspunkt. Dette kunngjøres på Facebook, med oppslag på de aktuelle stedene og på vår egen
		Facebook side: <a href="https://www.facebook.com/profile.php?id=61571948758888"
			>Brukthallen Flekkefjord.</a
		><br />
		<em>Merk: Vi kan dessverre ikke ta imot senger, madrasser eller hvitevarer. </em>
	</p>
	<p>Takk for at du velger Brukthallen og dermed støtter bygging av det nye Kirketorget!</p>
</Section>

<Section title="Kontakt Oss">
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
</Section>

<style lang="postcss">
	@reference "tailwindcss";

	section {
		display: grid;
		grid-template-columns: subgrid;
		gap: 0.8rem;
		background-color: var(--bg);
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
