<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Housing Solutions</PageHeader>

<Entry bind:footnotes id="40%">
	<span slot="num">40%</span>
	<span slot="lead"
		>Life-cycle assessment (LCA) studies performed in the last decade on the use of cross-laminated
		timber (CLT) to construct multi-storey buildings &ndash; instead of more conventional steel and
		concrete &ndash; show a 40% reduction in carbon footprint.<FN
			{footnotes}
			desc="'Cross-laminated timber for building construction: A life-cycle-assessment overview'"
			url="https://www.sciencedirect.com/science/article/pii/S2352710222004958?via%3Dihub"
		/></span
	>
	<ul>
		<li>
			Advantages of using CLT include its low environmental impacts, its high strength-to-weight
			ratio, its ease of installation and its aesthetic appeal.
		</li>
		<li>
			CLT stores carbon during its service life. The panels can then be reused or recycled. (Being a
			relatively new technology, ClT buildings are still within their service life so how much reuse
			or recycling will be practicable is yet unknown.)
		</li>
		<li>
			CLT has been associated with a 30% reduction in construction time <FN
				{footnotes}
				desc="'A Project Contribution to the Development of Sustainable Multi-Storey Timber Buildings...'"
				url="https://repositorium.sdum.uminho.pt/handle/1822/26947"
			/>.
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
	/* dl {
		display: flex;
		flex-flow: row wrap;
		margin-top: 0.375em;
	} */
	/* dt {
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
	} */
</style>
