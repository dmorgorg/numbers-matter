<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Causes of Global Warming</PageHeader>

<Entry bind:footnotes id="11pc">
	<span slot="num">11%</span>
	<span slot="lead"
		>In 2018, building materials (especially steel, brick, and steel) were responsible for 11% of
		global greenhouse gas emissions.<FN
			{footnotes}
			desc="'Global greenhouse gas emissions from residential and commercial building materials and mitigation strategies to 2060'"
			accessed="15th November, 2023"
			url="https://www.nature.com/articles/s41467-021-26212-z"
		/>.</span
	>
	<ul>
		<li>
			Demand for new buildings is expected to rise rapidly, driven by increasing populations, and
			wealth in Africa and Asia and by demand for upgrades of urban housing stock.
		</li>
		<li>
			Building materials accounted for more than 50% of concrete production and 40% of steel
			production.
		</li>
		<li>
			The demand for increased building materials can be mitigated somewhat by using materials with
			less environmental impact, such as increased use of wood. Cross-laminated timber (CLT) shows
			promise, providing the strength of concrete for one-fifth the weight. <FN
				{footnotes}
				desc="'5 Benefits of Building with Cross-Laminated Timber'"
				accessed="15th November, 2023"
				url="https://cnr.ncsu.edu/news/2022/08/5-benefits-cross-laminated-timber/"
			/>. The use of wood locks in the carbon content for the life of the building. Despite advances
			in building technology, widespread use of less efficient building practices are still widely
			used, imposing a challenge in meeting global climate targets for GHG emissions.
		</li>
	</ul>
</Entry>

<Entry bind:footnotes id="11&22">
	<span slot="num">11% and 21%</span>
	<span slot="lead"
		>In 2022, coal accounted for about 11% of U.S energy consumption but 21% of energy-related CO<sub
			>2</sub
		>
		emissions, making coal the dirtiest energy of the coal, petroleum and natural gas fossil fuels triad
		<FN
			{footnotes}
			desc="'Energy and the environment explained.'"
			accessed="19th November, 2023"
			url="https://www.eia.gov/energyexplained/energy-and-the-environment/where-greenhouse-gases-come-from.php"
		/>.</span
	>
	<img
		src="/images/consumption&emissions.png"
		alt="fossil fuel consumption and associated CO2 emissions"
	/>
</Entry>
<Entry bind:footnotes id="32&34">
	<span slot="num">32% and 34%</span>
	<span slot="lead"
		>In 2022, natural gas accounted for about 32% of U.S energy consumption but 34% of
		energy-related CO<sub>2</sub>
		emissions <FN
			{footnotes}
			desc="'Energy and the environment explained.'"
			accessed="19th November, 2023"
			url="https://www.eia.gov/energyexplained/energy-and-the-environment/where-greenhouse-gases-come-from.php"
		/>.</span
	>
	<img
		src="/images/consumption&emissions.png"
		alt="fossil fuel consumption and associated CO2 emissions"
	/>
</Entry>

<Entry bind:footnotes id="36&46">
	<span slot="num">36% and 46%</span>
	<span slot="lead"
		>In 2022, petroleum accounted for about 36% of U.S energy consumption but 46% of energy-related
		CO<sub>2</sub>
		emissions <FN
			{footnotes}
			desc="'Energy and the environment explained.'"
			accessed="19th November, 2023"
			url="https://www.eia.gov/energyexplained/energy-and-the-environment/where-greenhouse-gases-come-from.php"
		/>.</span
	>
	<img
		src="/images/consumption&emissions.png"
		alt="fossil fuel consumption and associated CO2 emissions"
	/>
</Entry>
<Entry bind:footnotes id="57pc">
	<span slot="num">57%</span>
	<span slot="lead"
		>Clouds created by<TT
			tt={[
				'contrails',
				'Contrails are water <b>con</b>densation <b>trails</b> that are often visible as linear clouds behind airplanes. They are caused by water vapour in the air condensing around soot and other particles emitted from the jet engines in cold air (below about -40<sup>o</sup>C/-40<sup>o</sup>F). Under the right conditions, contrails can be hundreds of kilometres in length and exist for several hours.'
			]}
			maxWidth="x-wide"
		/> account for roughly 57% of aviation's global warming impact <FN
			{footnotes}
			desc="'Transport'"
			accessed="17th November, 2023"
			url="https://www.ipcc.ch/report/ar6/wg3/downloads/report/IPCC_AR6_WGIII_Chapter10.pdf"
		/>.</span
	>
	<ul>
		<li>
			Contrails that form cirrus clouds are not long-lived, in contrast to the CO<sub>2</sub> emissions
			from aviation. Night-time contrails add to global warming by trapping warmth that would otherwise
			escape. Daytime contrails can actually reduce warming by reflecting some of the sun's radiation
			that would otherwise reach the earth's surface.
		</li>
		<li>
			Aviation was grounded in the US for three days following the terrorist attacks on the World
			Trade Center on the 9th November, 2001, and the Pentagon. The diurnal temperature range (DTR)
			increased by <TT tt={['1<sup>o</sup>C', '1.8<sup>o</sup>F']} /> over the days before and the days
			after the grounding. It has been argued that the absence of contrails was responsible for the warmer
			days and cooler nights but it has also been argued that the change in DTR was not significant,
			and not out of line with other measured variability <FN
				{footnotes}
				desc="'9/11 research challenged: contrails aren't turning up the heat'"
				accessed="16th November, 2023"
				url="https://www.bbc.co.uk/blogs/climatechange/2009/05/911_contrails_study_challenged.html"
			/>
			<FN
				{footnotes}
				desc="'Contrails reduce daily temperature range'"
				accessed="16th November, 2023"
				url="https://www.nature.com/articles/418601a?error=cookies_not_supported&code=594c8287-a7a4-46c8-9583-f5cdd10d2dbc"
			/>.
		</li>
		<li>
			When short-lived climate forcers (SLCF) are considered (contrails, nitrous oxide, soot, water
			vapour and black carbon), they amount to two-thirds of aviation's climate impact <FN
				{footnotes}
				desc="'Airline contrails warm the planet twice as much as CO2, EU study finds'"
				accessed="17th November, 2023"
				url="https://www.transportenvironment.org/discover/airline-contrails-warm-planet-twice-much-co2-eu-study-finds/"
			/>. That is, these SLCFs warm the planet twice as much as does the associated CO<sub>2</sub>,
			vapour and black carbon), they amount to two-thirds of aviation's climate impact. That is,
			these SLCFs warm the planet twice as much as does the associated CO<sub>2</sub>. Aviation
			warms the planet three times more than the emitted CO<sub>2</sub> would indicate.
		</li>
	</ul>
</Entry>

<Entry bind:footnotes id="2bn">
	<span slot="num"><TT tt={['2.00bn tonnes', '1.97bn (long) tons']} /></span>
	<span slot="lead"
		>Greenhouse gas emissions dipped by a mere <TT tt={['2.00bn tonnes', '1.97bn (long) tons']} /> while
		most of us were confined to our homes in 2020 due to the Covid-19 pandemic <FN
			{footnotes}
			desc="'Greenhouse gas emissions, 2021. Our World in Data.'"
			accessed="13th November, 2023"
			url="https://ourworldindata.org/greenhouse-gas-emissions"
		/>.</span
	>
	<ul>
		<li>
			International air travel dropped by 60% in 2020 due to the pandemic <FN
				{footnotes}
				desc="'2020 passenger totals drop 60 per cent...'"
				accessed="14th November, 2023"
				url="https://www.icao.int/Newsroom/Pages/2020-passenger-totals-drop-60-percent-as-COVID19-assault-on-international-mobility-continues.aspx"
			/>. Yet worldwide greenhouse gas emissions dropped by less than 4% (2.00/54.6=3.66%). We can
			not make a serious dent in our emissions, let alone get to net zero, on the back of reduced
			air travel. Air travel (domestic and international, passenger and freight) contributes 1.9% of
			greenhouse gas emissions (2016 data), or 2.5% of CO<sub>2</sub> emissions (2018 data) <FN
				{footnotes}
				desc="'Our World in Data.'"
				accessed="14th November, 2023"
				url="https://ourworldindata.org/co2-emissions-from-aviation"
			/>.
		</li>
		<li>
			It is widely accepted that aviation has a considerable warming effect over and above that due
			to CO<sub>2</sub> alone. Three times as much <FN
				{footnotes}
				desc="this site..."
				accessed="14th November, 2023"
				url="https://numbers-matter.org/climate/problems/warming/causes#57%"
			/> - so airline travel may not be as benign as it appears.
		</li>
	</ul>
</Entry>

<Entry bind:footnotes id="54.6bn">
	<span slot="num"><TT tt={['54.6bn tonnes', '53.7bn (long) tons']} /></span>
	<span slot="lead"
		>Greenhouse gas emissions for 2021 are <TT tt={['54.6bn tonnes', '53.7bn (long) tons']} />, up
		more than thirteen-fold from <TT tt={['4.0bn tonnes', '3.94bn (long) tons']} maxWidth="wide" /> in
		1850 <FN
			{footnotes}
			desc="'Greenhouse gas emissions, 2021. Our World in Data.'"
			accessed="12th November, 2023"
			url="https://ourworldindata.org/greenhouse-gas-emissions"
		/>.</span
	>
	<ul>
		<li>
			Most of the news we hear about climate change involves carbon dioxide in the atmosphere but CO<sub
				>2</sub
			> is only the largest of the emissions contributing to global warming. Other greenhouse gases that
			have added to global warming include methane and nitrous oxide.
		</li>
		<li>
			Analysing emissions by country is not a useful metric. A country's emissions are influenced by
			both the emissions per capita and the population. We hear a lot about China's and India's high
			emissions: China's (<TT tt={['13.7bn tonnes', '13.5bn (long) tons']} /> in 2021) are much higher
			than those of the United States (<TT tt={['5.93bn tonnes', '5.84bn (long) tons']} /> in 2021).
			But greenhouse gases don't stop at international borders: we need to think in terms of what each
			of us emits worldwide. On a per capita basis, China is far from the worst emissions offender.
		</li>
		<li>
			Some per capita figures for greenhouse gas emissions in 2021:
			<dl class="bold">
				<dt>Country</dt>
				<dd>Per capita emissions <br />(billion tonnes)</dd>
			</dl>
			<dl>
				<dt>Mongolia</dt>
				<dd>27.9</dd>

				<dt>Canada</dt>
				<dd>20.4</dd>

				<dt>United States</dt>
				<dd>17.6</dd>

				<dt>China</dt>
				<dd>9.62</dd>

				<dt>United Kingdom</dt>
				<dd>6.26</dd>

				<dt>India</dt>
				<dd>2.77</dd>
			</dl>
		</li>

		<li>
			Almost certainly, India's emissions will grow at a faster rate than ours in the prosperous
			'West.' But we are responsible for causing most of the global warming problem, filling the
			atmosphere with greenhouse gases; who are we now to say, from our comfortable homes with our
			multiple vehicles, that the poor in India don't deserve electric lights and refrigerators?
		</li>
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
	dl {
		display: flex;
		flex-flow: row wrap;
		margin-top: 0.375em;
	}
	dt {
		flex-basis: 35%;
		padding: 0.05em 0.5em;

		text-align: right;
		color: black;
	}
	dd {
		flex-basis: 55%;
		flex-grow: 1;
		margin: 0;
		padding: 0.05em 1em;
	}
	.bold {
		font-weight: bold;
	}
	img {
		border: 1px solid black;
	}
</style>
