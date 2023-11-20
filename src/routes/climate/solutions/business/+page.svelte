<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Solutions for Business</PageHeader>

<Entry {footnotes} id="54%">
	<span slot="num">54%</span>
	<span slot="lead"
		>Up to 54% of work's carbon footprint may be eliminated by full-time working from home (WFH).
		Savings from less than full-time are disproportionately smaller <FN
			{footnotes}
			desc="'Climate mitigation potentials of teleworking are sensitive to changes in lifestyle and workplace rather than ICT usage'"
			accessed="20th November, 2023"
			url="https://www.pnas.org/doi/full/10.1073/pnas.2304099120"
		/>.
	</span>
	<ul>
		<li>
			Hybrid workers, spending 2 to 4 days at home, reduce GHG emissions by 11 to 29%. This is
			mainly due to less office energy use and less commuting. One day a week hybrid workers only
			save 2% GHG.
		</li>
		<li>
			Results are influenced by many factors. Hybrid workers tend to live further from their work
			than do onsite workers. Remote workers tend to travel more for non-commute activities than do
			their onsite counterparts, e.g. for exercise, recreational activities, socialising, etc. WFH
			requires extra space at home which may result in extra residential energy consumptions. Remote
			households own more vehicles.
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
		}
	}
	img {
		margin: 0.5em;
	}
</style>
