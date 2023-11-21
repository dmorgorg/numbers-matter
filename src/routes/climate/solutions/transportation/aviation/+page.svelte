<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Aviation Solutions</PageHeader>

<Entry bind:footnotes id="54pc">
	<span slot="num">54%</span>
	<span slot="lead"
		>Aviation contributes more to global warming than heating due just to CO<sub>2</sub> emissions;
		contrails and other short-lived climate forcers (SLCFs) <b>triple</b> the heating effect <FN
			{footnotes}
			desc="'Using Google AI to help airlines prevent contrails'"
			accessed="16th November, 2023"
			url="https://sites.research.google/contrails/"
		/>. Google, using artificial intelligence (AI), has predicted routes over the US that avoid the
		conditions that create contrails. After 70 test flights, it was found that these predictions
		reduced contrails by 54% compared with flights that didn't use the predictions <FN
			{footnotes}
			desc=" Page within this site:"
			accessed="16th November, 2023"
			url="https://numbers-matter.org/climate/problems/warming/causes#57%"
		/>.</span
	>
	<ul>
		<li>
			Flights avoiding contrails used 2% more fuel but, since not all flight create contrails, this
			amounted to about 0.3% over a typical airline fleet. Contrail avoidance costs would be in the
			range of $5-25/ton of CO<sub>2</sub>, a cost-effective solution.
		</li>
		<li>
			On average, only 15% of flights in the contiguous United States generate contrails. Contrails
			are concentrated in south-east and mid-west, and on the Pacific coast, and are twice as likely
			between the months of June and September. Ice-supersaturated (ISS) regions where contrails
			form tend to be wide but only a few hundred metres/yards tall.
			<div class="width70"><img src="/images/iss.jpg" alt="iss" /></div>
			<div class="caption">
				ISSR, at <TT tt={['22,500m', "36,000'"]} />, 9:00 am on November 15th 2014 <FN
					{footnotes}
					desc="'Reducing global warming by airline contrail avoidance: A case study of annual benefits for the contiguous United States'"
					accessed="16th November, 2023"
					url="https://www.sciencedirect.com/science/article/pii/S2590198219300338#f0010"
				/>.
			</div>
			Flying around ISS areas is not cost effective but flying over them has benefits.
		</li>
	</ul>
</Entry>

<Entry bind:footnotes id="92pc">
	<span slot="num">92%</span>
	<span slot="lead"
		>Aviation is responsibe for about 6% of the globe's warming. Contrails cause a large part of
		that heating. Flying above ice supersaturated regions where contrails form, rather than through
		them, can reduce the warming effects by as much as 92% for the United States. <FN
			{footnotes}
			desc="'Reducing global warming by airline contrail avoidance: A case study of annual benefits for the contiguous United States'"
			accessed="17th November, 2023"
			url="https://www.sciencedirect.com/science/article/pii/S2590198219300338"
		/>.
	</span>
	<ul>
		<li>
			A daily decrease of 63% of net radiative forcing (NRF) is predicted for increases in elevation
			of <TT tt={['600m', "2000'"]} /> and a decrease of 92% for an increase in elevation of <TT
				tt={['1200m', "4000'"]}
			/>. In addition to route optimization for winds, routes should be also optimized for contrail
			avoidance.
		</li>
		<li>
			The increase in fuel burnt due to the elevation gain is not significant due to lower drag at
			higher altitudes.
		</li>
		<li>
			A different study <FN
				{footnotes}
				desc="'Small altitude changes could cut contrail impact of flights by up to 59 per cent'"
				accessed="17th November, 2023"
				url="https://www.imperial.ac.uk/news/195294/small-altitude-changes-could-contrail-impact/"
			/> from Imperial College, London, examined Japan's airspace and determined that just 2% of flights
			were responsible for 80% of climate forcing in the airspace and that an increase or decrease in
			altitude of around 1.7% could reduce the contrail climate forcing by 59%.
		</li>
	</ul>
</Entry>
