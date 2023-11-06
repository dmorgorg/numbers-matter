<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Carbon Capture and Storage (CCS)</PageHeader>

<Entry {footnotes}>
	<span slot="num">42</span>
	<span slot="lead"
		>We all<FN {footnotes} desc="that's us" url="https://example.com" />know this is the answer
	</span>
	<ul>
		<li>
			A proven, cheap and effective method for extracting CO<sub>2</sub> is to plant trees.
		</li>
		<li>
			Various techniques are being developed to extract carbon directly from the atmosphere. Some
			are described on this page but most are, as yet, unproven and expensive. According to the
			Clean Air Task Force <FN
				{footnotes}
				desc="'A once-in-a-generation opportunity to control carbon pollution'"
				url="https://www.catf.us/2022/08/the-inflation-reduction-act-creates-a-whole-new-market-for-carbon-capture/"
			/>, there are no operational DAC facilities in the U.S. The only DAC plant in commercial
			operation is a single plant operation in Iceland.
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
</style>
