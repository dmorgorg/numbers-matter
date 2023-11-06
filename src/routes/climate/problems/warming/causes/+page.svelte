<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Causes of Global Warming</PageHeader>

<Entry bind:footnotes>
	<span slot="num"><TT tt={['54.6bn tonnes', '53.7bn (long) tons']} /></span>
	<span slot="lead"
		>Greenhouse gas emissions for 2021 are <TT tt={['54.6bn tonnes', '53.7bn (long) tons']} />, up
		more than thirteen-fold from <TT tt={['4.0bn tonnes', '3.94bn (long) tons']} /> in 1850 <FN
			{footnotes}
			desc="'Greenhouse gas emissions, 2021. Our World in Data.'"
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
			Almost ertainly, India's emissions will grow at a faster rate than ours in the prosperous
			'West.' But we are responsible for causing most of the global warming problem, filling the
			atmosphere with greenhouse gases; who are we now to say, from our comfortable homes with our
			multiple vehicles, that the poor in India don't deserve electric lights and refrigerators?
		</li>
	</ul>
</Entry>
<Entry bind:footnotes>
	<span slot="num"><TT tt={['2.00bn tonnes', '1.97bn (long) tons']} /></span>
	<span slot="lead"
		>Greenhouse gas emissions dipped by a mere <TT tt={['2.00bn tonnes', '1.97bn (long) tons']} /> while
		most of us were confined to our homes in 2020 due to the Covid-19 pandemic <FN
			{footnotes}
			desc="'Greenhouse gas emissions, 2021. Our World in Data.'"
			url="https://ourworldindata.org/greenhouse-gas-emissions"
		/>.</span
	>
	<ul>
		<li>
			International air travel dropped by 60% in 2020 due to the pandemic <FN
				{footnotes}
				desc="'2020 passenger totals drop 60 per cent...'"
				url="https://www.icao.int/Newsroom/Pages/2020-passenger-totals-drop-60-percent-as-COVID19-assault-on-international-mobility-continues.aspx"
			/>. Yet worldwide greenhouse gas emissions dropped by less than 4% (2.00/54.6=3.66%). We can
			not make a serious dent in our emissions, let alone get to net zero, on the back of reduced
			air travel. Air travel (domestic and international, passenger and freight) contributes 1.9% of
			greenhouse gas emissions (2016 data), or 2.5% of CO<sub>2</sub> emissions <FN
				{footnotes}
				desc="'Our World in Data.'"
				url="https://ourworldindata.org/co2-emissions-from-aviation"
			/>. This is not to suggest that reduced air travel will not help ameliorate global warming.
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
</style>
