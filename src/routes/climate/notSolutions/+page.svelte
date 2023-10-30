<script>
	import Entry from '$lib/components/Entry2.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
</script>

<PageHeader>Effects of Global Warming</PageHeader>
<Entry>
	<span slot="num">7m</span>
	<!-- leader="Global sea-level rise will be 
		22 feet
	 if/when the Greenland Ice Sheet disappears." -->

	<ul>
		<li>
			It won't all happen at once; <TT tt={['WWS', 'Wind, water and solar']} /> you'll have time to pack
			up your beachfront home.
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
