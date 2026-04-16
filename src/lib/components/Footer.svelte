<footer>
	<p>Brukthallen flekkefjord er drevet av foreningen «Kirketorgets venner»</p>
</footer>

<style>
	footer {
		grid-column: full;
		display: grid;
		grid-template-columns: subgrid;
		place-content: center;
		padding-block: 1rem;
		background-color: var(--base-clr);
		color: var(--color-emerald-100);
		text-align: center;

		p {
			grid-column: content;
		}
	}
</style>
