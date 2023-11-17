<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Aviation Solutions</PageHeader>

<Entry bind:footnotes id="54%">
	<span slot="num">54%</span>
	<span slot="lead"
		>Aviation contributes more to global warming than heating due just to CO<sub>2</sub> emissions;
		contrails and other short-lived climate forcers (SLCFs) <b>triple</b> the heating effect <FN
			{footnotes}
			desc="'Using Google AI to help airlines prevent contrails'"
			url="https://sites.research.google/contrails/"
		/>. Google, using artificial intelligence (AI), has predicted routes over the US that avoid the
		conditions that create contrails. After 70 test flights, it was found that these predictions
		reduced contrails by 54% compared with flights that didn't use the predictions <FN
			{footnotes}
			desc=" Page within this site: <br/>"
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
			between the months of June and September. Ice-supersaturated (ISS) areas where contrails form
			tend to be wide but only a few hundred metres/yards tall.
			<div class="width70"><img src="/images/iss.jpg" alt="iss" /></div>
			<div class="caption">
				ISSR, at <TT tt={['22,500m', "36,000'"]} />, 9:00 am on November 15th 2014 <FN
					{footnotes}
					desc="'Reducing global warming by airline contrail avoidance: A case study of annual benefits for the contiguous United States'"
					url="https://www.sciencedirect.com/science/article/pii/S2590198219300338#f0010"
				/>.
			</div>
			Flying around ISS areas is not cost effective but flying over them has benefits.
		</li>
		<li>
			An analysis performed by the National Airspace System (NAS) found an elevation gain of <TT
				tt={['600m', "2000'"]}
			/>, flying over ISS areas,
		</li>
	</ul>
</Entry>

<style lang="postcss">
	ul {
		list-style-type: disc;
		margin-top: 1em;
		margin-left: 2em;

		li {
			margin-bottom: 0.5em;

			img {
				width: 70%;
				margin: 0.5em auto;
				margin-bottom: 0;
			}
			.caption {
				font-size: 90%;
				text-align: center;
				margin-bottom: 0.5em;
			}
		}
	}
</style>
