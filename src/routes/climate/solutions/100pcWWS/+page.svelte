<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Going 100% wind, water and solar...</PageHeader>

<Entry bind:footnotes id="57pc">
	<span slot="num">57%</span>
	<span slot="lead"
		>A total (United States) transition from business as usual (BAU) energy to wind-water-solar
		(WWS) by 2050 would result in the doubling of electricity demand but would reduce total end-use
		energy demand by 57% compared with BAU <FN
			{footnotes}
			desc="'Zero air pollution and zero carbon from all energy at low cost and
		without blackouts in variable weather throughout the U.S. with 100%
		wind-water-solar and storage'"
			accessed="19th November, 2023"
			url="https://web.stanford.edu/group/efmh/jacobson/Articles/I/21-USStates-PDFs/21-USStatesPaper.pdf"
		/>.
	</span>

	<ul>
		<li>
			Energy costs would be approximately 63% less under a WWS scenario (or approximately 86% when
			the reduced climate and pollution-related health care costs are included).
		</li>
		<li>
			Reductions in end use energy demand are mostly due to moving from natural gas air and water
			heaters to heat pumps, from internal combustion engines (ICE) to electric vehicles (EV) and
			the elimination of the need to mine conventional fuels.
		</li>
		<li>
			Not only is less energy required with 100% WWS and storage compared to BAU fossil-fuel
			generation, the energy will, on average, cost less: 11% less in California; 21% less in New
			York, 27% less in Texas and 1.5% higher in Florida.
		</li>
		<li>
			Mark Jacobson has come under criticism for being overly optimistic in his assertions that a
			transition wholly to renewables can be managed. A group of 21 academics (Clack et al.)
			published a paper outlining flaws in Jacobson's methodology <FN
				{footnotes}
				desc="'Evaluation of a proposal for reliable low-cost grid power with 100% wind, water, and solar'"
				accessed="19th November, 2023"
				url="https://www.pnas.org/doi/full/10.1073/pnas.1610381114"
			/>. Jacobson promptly sued for $10 million, then withdrew his suit <FN
				{footnotes}
				desc="'Column: A Stanford professor drops his ridiculous defamation lawsuit against his scientific critics'"
				accessed="19th November, 2023"
				url="https://www.latimes.com/business/hiltzik/la-fi-hiltzik-jacobson-lawsuit-20180223-story.html"
			/>. He published a rebuttal to the 'errors' pointed out in Clack et al., which "are
			demonstrably false." <FN
				{footnotes}
				desc="'Jacobson response'"
				accessed="19th November, 2023"
				url="https://s3.documentcloud.org/documents/4247258/Jacobson-Response.pdf"
			/>. The significance of the 'errors,' if any, remains slight. A main contention is that
			Jacobson does not use nuclear power, carbon capture and storage (CCS) and bioenergy to reach
			his goal of a 100% renewable and reliable grid.
		</li>
	</ul>
</Entry>

<Entry bind:footnotes id="4.7mill">
	<span slot="num">4.7 million</span>
	<span slot="lead"
		>Transitioning to 100% WWS and storage in the US will provide a net increase of up to 4.7
		million permanent jobs <FN
			{footnotes}
			desc="'Zero air pollution and zero carbon from all energy at low cost and
		without blackouts in variable weather throughout the U.S. with 100%
		wind-water-solar and storage'"
			accessed="19th November, 2023"
			url="https://web.stanford.edu/group/efmh/jacobson/Articles/I/21-USStates-PDFs/21-USStatesPaper.pdf"
		/>. This transition is far more aggressive than those the Paris agreement calls for but are
		still technically feasible.
	</span>

	<!-- <ul>
		<li />
		<li />
	</ul> -->
</Entry>

<Entry bind:footnotes id="42.5pc">
	<span slot="num">42.5%</span>
	<span slot="lead"
		>A total transition, of 139 countries, from business as usual (BAU) energy to wind-water-solar
		(WWS) by 2050 would result in the reduction of end-use energy demand by 42.5% <FN
			{footnotes}
			desc="'100% Clean and Renewable Wind, Water, and Sunlight All-Sector Energy Roadmaps for 139 Countries of the World'"
			accessed="19th November, 2023"
			url="https://www.sciencedirect.com/science/article/pii/S2542435117300120"
		/>. These transitions are far more aggressive than those the Paris agreement <FN
			{footnotes}
			desc="''"
			accessed="19th November, 2023"
			url="https://www.nrdc.org/stories/paris-climate-agreement-everything-you-need-know#sec-whatis"
		/> calls for but are still technically feasible.
	</span>

	<ul>
		<li>
			Energy costs would be approximately 63% less under a WWS scenario (or approximately 86% when
			the reduced climate and pollution-related health care costs are included).
		</li>
	</ul>
</Entry>

<Entry bind:footnotes id="51.3trill">
	<span slot="num">$51.3 trillion/year</span>
	<span slot="lead"
		>A total transition, of 139 countries, from BAU energy to WWS by 2050 would also result in <FN
			{footnotes}
			desc="''"
			accessed="19th November, 2023"
			url="https://www.nrdc.org/stories/paris-climate-agreement-everything-you-need-know#sec-whatis"
		/>:
		<ul>
			<li>The creation of 24.3 million permanent full-time jobs,</li>
			<li>
				The avoidance of 4.6 million/year premature air-pollution deaths (3.5 million/year by 2050),
			</li>
			<li>
				A reduction of $22.8 trillion/year in air pollutions costs and $28.5 trillion/year in
				climate costs for a combined <b>$51.3</b> trillion/year.
			</li>
		</ul>
	</span>
	<img src="/images/42point5.jpg" alt="42.5%" />
</Entry>

<style>
	img {
		border: 2px solid black;
	}
</style>
