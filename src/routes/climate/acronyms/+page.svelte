<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Acronyms Used</PageHeader>

<div class="container">
	<dl>
		<dt>CCS</dt>
		<dd>Carbon Capture and Storage</dd>
	</dl>
	<dl>
		<dt>CDR</dt>
		<dd>Carbon Dioxide Removal</dd>
	</dl>
	<dl>
		<dt>DAC</dt>
		<dd>Direct Air Capture</dd>
	</dl>
	<dl>
		<dt>ERW</dt>
		<dd>Earth Rock Weathering</dd>
	</dl>
	<dl>
		<dt>GMT</dt>
		<dd>Global Mean Temperature</dd>
	</dl>
	<dl>
		<dt>GRF</dt>
		<dd>Glacial Rock Flour</dd>
	</dl>
	<dl>
		<dt>SLR</dt>
		<dd>Sea Level Rise</dd>
	</dl>
</div>

<style lang="postcss">
	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		width: 70%;
		margin: 0 auto;
	}
	dl {
		display: flex;
		flex-flow: row wrap;
		/* border: solid #333;
		border-width: 1px 1px 1px 0; */
		margin-top: 0.375em;
	}
	dt {
		flex-basis: 20%;
		padding: 0.05em 0.5em;
		@apply bg-tertiary-400;
		@apply rounded-s-full;
		/* border-top-left-radius: 0.375em;
		border-bottom-left-radius: 0.375em; */

		text-align: right;
		color: black;
	}
	dd {
		flex-basis: 70%;
		flex-grow: 1;
		margin: 0;
		padding: 0.05em 1em;
		/* border: solid #333;
		border-width: 1px 1px 1px 0; */
		@apply bg-tertiary-50;
		border-left: 0.5em solid white;
		@apply rounded-e-full;
	}
</style>
