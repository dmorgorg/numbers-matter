<script>
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
</script>

<PageHeader>Effects of Global Warming</PageHeader>
<Entry>
	<span slot="num"><TT tt={['7m', '23 feet']} /></span>
	<span slot="lead"
		>The Greenland ice cap is melting. If it all melts, global sea-levels will rise by about <TT
			tt={['7m', '23 feet']}
		/>.</span
	>
	<ul>
		<li>
			The good news is that it won't all happen at once; the rise will be gradual, allowing plenty
			of time to pack up your beachfront home and move inland.
		</li>
	</ul>
</Entry>

<style>
	ul {
		list-style-type: disc;
		margin-top: 1em;
		margin-left: 2em;
	}
</style>
