<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Acronyms Used</PageHeader>

<div class="container">
	<div class="acronyms">
		<div class="acronym">
			<span class="short">DAC:</span>
			<span class="long">Direct Air Capture</span>
		</div>
	</div>
</div>

<style>
	.container {
		display: flex;
		justify-content: center;
	}
	.acronyms {
		display: flex;
		flex-direction: column;
	}
</style>
