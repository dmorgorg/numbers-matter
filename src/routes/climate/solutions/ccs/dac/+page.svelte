<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Direct Air Capture (DAC)</PageHeader>

<Entry {footnotes} headless={true}>
	<b>Direct air capture</b> uses technologies that remove CO<sub>2</sub> from the atmosphere, thereby
	extracting carbon previously emitted into the atmosphere by industrial processes, forest fires, etc...
</Entry>

<Entry {footnotes}>
	<span slot="num"><TT tt={['1.5<sup>o</sup>C', '2.7<sup>o</sup>F']} /></span>
	<span slot="lead"
		>In order to limit global warming to<TT tt={['<b>1.5<sup>o</sup>C</b>', '2.7<sup>o</sup>F']} /> above
		preindustrial temperatures, reducing greenhouse gas emissions alone is insufficient. Despite transitions
		towards lower emissions already underway, few are consistent with limiting warming sufficiently.
		Carbon dioxide removal (CDR) from the atmosphere will also be necessary.<FN
			{footnotes}
			desc="What Transitions could Enable Limiting Global Warming to 1.5°C?"
			url="https://www.ipcc.ch/sr15/faq/faq-chapter-4/"
		/>
	</span>
	<ul>
		<li>
			A time-proven, cheap and effective method for extracting CO<sub>2</sub> is to
			<b>plant trees</b>!
		</li>
		<li>
			Various techniques are being developed to extract carbon directly from the atmosphere. This
			process is known as direct air capture (DAC). Some are described on this page but most are, as
			yet, unproven and expensive.
			<!-- According to the Clean Air Task Force <FN
				{footnotes}
				desc="'A once-in-a-generation opportunity to control carbon pollution'"
				url="https://www.catf.us/2022/08/the-inflation-reduction-act-creates-a-whole-new-market-for-carbon-capture/"
			/>, there are no operational DAC facilities in the U.S. The only DAC plant in operation world
			wide is Orca, in Iceland. -->
		</li>
	</ul>
</Entry>

<Entry {footnotes}>
	<span slot="num"><TT tt={['728 kg/ha', '650 lb/ac']} /></span>
	<span slot="lead"
		>Glacial rock flour (GRF) is produced (about one billion tonnes annually) by the glacial erosion
		- or 'grinding' - of rocks beneath the Greenland ice sheet. This GRF can then be spread on
		fields where it increases crop yields. It can also absorb<TT
			tt={['<b>728 kg/ha</b>', '650 lb/ac']}
		/> of CO<sub>2</sub> from the atmosphere over a period of three years.<FN
			{footnotes}
			desc="'Quantification of CO2 uptake by enhanced weathering of silicate minerals applied to acidic soils.'<br/>"
			url="https://www.sciencedirect.com/science/article/pii/S1750583623000427?via%3Dihub#bib0021"
		/></span
	>
	<ul>
		<li>
			The estimated <TT tt={['728 kg/ha', '650 lb/ac']} /> CO<sub>2</sub> results from the
			application of <TT tt={['<b>50 tonnes/ha</b>', '20 tons/ac']} /> of Greenlandic
			<!-- <FN
				{footnotes}
				desc="'IPCC Special Report: Global Warming of 1.5<sup>o</sup>C.'<br/>"
				url="https://www.ipcc.ch/sr15/chapter/spm/"
			/>  -->
			glacial rock flour to acidic sandy soil in Denmark. This uses a process known as enhanced rock
			weathering (ERW).
		</li>
		<li>
			In tests held in Denmark in 2019, <TT
				tt={['<b>10</b> and <b>50 tonnes/ha</b>', '4.1 and 20.3 ton/ac']}
			/> of
			<TT tt={['GRF', 'Glacial rock flour']} /> were added to crops of maize and potato. Maize yields
			increased by 24% and potato yields by 19% for the year of application of GRF. No yield improvements
			were noted in subsequent years although carbon sequestration continued.
		</li>
		<!-- <li>( ͠° ͟ʖ ͡° )</li> -->
	</ul>
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
</style>
