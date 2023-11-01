<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Direct Air Capture (DAC)</PageHeader>
<Entry>
	<span slot="num"><TT tt={['1.5<sup>o</sup>C', '2.7<sup>o</sup>F']} /></span>
	<span slot="lead"
		>In order to limit global warming to<TT tt={['1.5<sup>o</sup>C', '2.7<sup>o</sup>F']} />, carbon
		dioxide removal (CDR) will be necessary.
		<FN
			{footnotes}
			desc="'IPCC Special Report: Global Warming of 1.5<sup>o</sup>C.'<br/>"
			href="https://www.ipcc.ch/sr15/chapter/spm/"
		/>
	</span>
	<ul>
		<li>
			test<FN
				{footnotes}
				desc="'IPCC Special Report: Global Warming of 1.5<sup>o</sup>C.'<br/>"
				href="https://www.ipcc.ch/sr15/chapter/spm/"
			/>
		</li>
	</ul>
	<div class="container">
		<div class="footnotes">
			{#if footnotes.length === 1}
				<h1>Reference:</h1>
			{:else if footnotes.length > 1}
				<h1>References:</h1>
			{/if}

			{#each footnotes as note, i}
				<div class="footnote">
					[{i + 1}] {@html note[0]}
					<a href={note[1]}>{note[2]}</a>
				</div>
			{/each}
		</div>
	</div>
</Entry>
<Entry>
	<span slot="num"><TT tt={['1bn tonnes', '1.1bn tons']} /></span>
	<span slot="lead"
		>One billion tonnes of glacial rock flour (GRF) is produced annually by the glacial erosion (or
		'grinding') of rocks beneath the Greenland ice sheet. This GRF can then be spread on fields
		where it both increases crop yields and absorbs carbon dioxide from the atmosphere.</span
	>
	<ul>
		<li>
			An estimated <TT tt={['728 kg/ha', '650 lb/ac']} /> CO<sub>2</sub> may be captured from the
			atmosphere after the application of <TT tt={['50 tonnes/ha', '20 tons/ac']} /> of Greenlandic glacial
			rock flour to acidic sandy soil in Denmark over a period of three years.
			<FN
				{footnotes}
				desc="'Quantification of CO2 uptake by enhanced weathering of silicate minerals applied to acidic soils.'<br/>"
				href="https://www.sciencedirect.com/science/article/pii/S1750583623000427?via%3Dihub#bib0021"
			/>
		</li>
		<li>
			In tests held in Denmark in 2019, <TT tt={['10 and 50 tonnes/ha', '4.1 and 20.3 ton/ac']} /> of
			<TT tt={['GRF', 'Glacial rock flour']} /> were added to crops of maize and potato. Maize yields
			increased by 24% and potato yields by 19% for the year of application of GRF. No long term improvements
			were noted.
			<FN
				{footnotes}
				desc="'Greenlandic glacial rock flour improves crop yield in organic agricultural production.'<br/>"
				href="https://link.springer.com/article/10.1007/s10705-023-10274-0"
			/>
		</li>
	</ul>
	<div class="container">
		<div class="footnotes">
			{#if footnotes.length === 1}
				<h1>Reference:</h1>
			{:else if footnotes.length > 1}
				<h1>References:</h1>
			{/if}

			{#each footnotes as note, i}
				<div class="footnote">
					[{i + 1}] {@html note[0]}
					<a href={note[1]}>{note[2]}</a>
				</div>
			{/each}
		</div>
	</div>
</Entry>

<style lang="postcss">
	ul {
		list-style-type: disc;
		margin-top: 1em;
		margin-left: 2em;
	}
	li {
		margin-bottom: 0.5em;
	}
	.container {
		width: 80%;
		margin: 0 auto;
		display: flex;
		justify-content: center;
		padding-top: 1em;

		.footnotes {
			display: flex;
			flex-direction: column;
			align-self: center;
			align-items: flex-start;
			/* font-size: 80%; */
			@apply text-tertiary-500;
			align-items: flex-start;

			h1 {
				color: black;
				text-decoration: underline;
				margin-bottom: 0.25em;
				align-self: center;
			}

			.footnote {
				font-size: 85%;
				padding-left: 1.5em;
				text-indent: -1.5em;
			}
		}
	}
</style>
