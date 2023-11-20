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

<Entry {footnotes} id="1.5C">
	<span slot="num"><TT tt={['1.5<sup>o</sup>C', '2.7<sup>o</sup>F']} /></span>
	<span slot="lead"
		>In order to limit global warming to<TT tt={['<b>1.5<sup>o</sup>C</b>', '2.7<sup>o</sup>F']} /> above
		preindustrial temperatures, reducing greenhouse gas emissions alone is insufficient. Despite transitions
		towards lower emissions already underway, few are consistent with limiting warming sufficiently.
		Carbon dioxide removal (CDR) from the atmosphere will also be necessary.<FN
			{footnotes}
			desc="What Transitions could Enable Limiting Global Warming to 1.5°C?"
			accessed="5th November, 2023"
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

<Entry {footnotes} id="728">
	<span slot="num"><TT tt={['728 kg/ha', '650 lb/ac']} /></span>
	<span slot="lead"
		>Glacial rock flour (GRF) is produced (about one billion tonnes annually) by the glacial erosion
		- or 'grinding' - of rocks beneath the Greenland ice sheet. This GRF can then be spread on
		fields where it increases crop yields. It can also absorb<TT
			tt={['<b>728 kg/ha</b>', '650 lb/ac']}
		/> of CO<sub>2</sub> from the atmosphere over a period of three years.<FN
			{footnotes}
			desc="'Quantification of CO2 uptake by enhanced weathering of silicate minerals applied to acidic soils.'"
			accessed="8th November, 2023"
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
			In tests held in Denmark in 2019, <TT tt={['10 and 50 tonnes/ha', '4.1 and 20.3 ton/ac']} /> of
			GRF were applied to fields planted with crops of maize and potato. Maize yields increased by 24%
			and potato yields by 19% for the year of application of GRF. No yield improvements were noted in
			subsequent years although carbon sequestration continued. <FN
				{footnotes}
				desc="Greenlandic glacial rock flour improves crop yield in organic agricultural production"
				accessed="8th November, 2023"
				url="https://link.springer.com/article/10.1007/s10705-023-10274-0"
			/>
		</li>
		<!-- <li>(° ͟ʖ°)</li> -->
		<!-- <li>
			Tests in less fertile soil in Ghana have seen greater yield increases but transportation of GRF
			for long distances becomes more of a factor.
		</li> -->
	</ul>
</Entry>

<Entry {footnotes} id="4000C">
	<span slot="num"><TT tt={['4,000 tonnes', '3900 (long) tons']} /></span>
	<span slot="lead"
		>In September, 2021, Climeworks launched the world's first direct air capture plant in
		Hellisheidi, Iceland. This plant (named Orca) has an annual CO<sub>2</sub> capture of up to <TT
			tt={['4,000 tonnes', '3900 (long) tons']}
		/>
		<FN
			{footnotes}
			desc="'From vision to reality: Orca is launched.'"
			accessed="8th November, 2023"
			url="https://climeworks.com/plant-orca"
		/></span
	>
	<ul>
		<li>
			The plant uses fans to draw air through filters which collect the CO<sub>2</sub>. When the
			filter is full, the temperature is raised, releasing concentrated CO<sub>2</sub> which is then
			captured, mixed with water and injected underground where it turns to rock in a couple of years.
		</li>

		<li>
			Iceland has abundant clean geothermal fuel so there is no CO<sub>2</sub> associated with powering
			and heating the plant.
		</li>
		<li>
			The plant cost between $10 million and $15 million to build and captures the emissions of
			approximately 250 US residents. Individuals can purchase carbon offsets for around $1200/ton.
			Bulk purchases are closer to $600/ton. <FN
				{footnotes}
				desc="'World’s Largest Carbon-Sucking Plant Starts Making Tiny Dent in Emissions'"
				accessed="8th November, 2023"
				url="https://www.bloomberg.com/news/features/2021-09-08/inside-the-world-s-largest-direct-carbon-capture-plant"
			/>
		</li>
		<li>
			Global CO<sub>2</sub> emissions for 2022 were <TT
				tt={['37.1bn tonnes', '36.5 (long) tons']}
			/>
			<FN
				{footnotes}
				desc="'Global CO2 emissions from fossil fuels'"
				accessed="8th November, 2023"
				url="https://ourworldindata.org/co2-emissions#global-co2-emissions-from-fossil-fuels-global-co2-emissions-from-fossil-fuels"
			/> That works out to be <TT tt={['1180 tonnes/min', '1160 (long) tons/min']} /> (37.1x10<sup
				>9</sup
			>/365/24/60/60/60). Each year, the Orca plant will remove slightly less than 3.5 minutes worth
			of current CO<sub>2</sub> emissions.
		</li>
	</ul>
</Entry>
<Entry {footnotes} id="$100">
	<span slot="num">$100/ton</span>
	<span slot="lead"
		>$100/ton is the Holy Grail of carbon pricing and startup Graphyte
		<FN
			{footnotes}
			desc="Graphyte"
			accessed="20th November, 2023"
			url="https://www.graphyte.com/"
		/> claims to reach that with its carbon-casting technique. Graphyte has backing from Bill Gates'
		Breakthrough Energy Ventures.
		<div class="width70">
			<img src="/images/carbonCasting.jpg" alt="carbon casting blocks" />
		</div></span
	>
	<ul>
		<li>
			Plant residues from timber and farming operations are frequently left to decompose, thereby
			releasing their stored CO<sub>2</sub> into the atmosphere and contributing the climate change.
			Carbon-casting aims to curtail that release. Graphyte claims to remove carbon from the atmosphere
			but it might be more accurate to claim that it is reducing the release of carbon into the atmosphere.
		</li>
		<li>
			Graphyte takes waste biomass (discarded wood residue, rice hulls, ...), dries and sterilizes
			it to prevent decomposition, condenses the material into dense carbon blocks which are then
			wrapped in a polymer barrier and stored underground. More or less indefinitely <FN
				{footnotes}
				desc="Bill Gates-Backed Startup to Use Old Wood to Remove Carbon From the Air"
				accessed="20th November, 2023"
				url="https://www.bloomberg.com/news/articles/2023-11-13/bill-gates-backed-startup-uses-old-wood-to-remove-carbon-from-air?embedded-checkout=true"
			/>.
		</li>
		<li>
			This process uses about one-tenth of the energy that most direct air capture methods require.
			The company is building its first plant in Arkansas, close to timber and rice mills for source
			materials. It projects to have the capacity to store 50,000 tons per year by July 2024.
		</li>
	</ul>
</Entry>

<style>
	img {
		border: 1px solid black;
	}
</style>
