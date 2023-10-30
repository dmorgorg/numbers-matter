<script>
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
</script>

<PageHeader>Effects of Global Warming</PageHeader>
<Entry>
	<span slot="num"><TT tt={['7m', '23 feet']} /></span>
	<span slot="lead"
		>The Greenland ice sheet is melting. We are on track for it all to melt. If/when that happens,
		mean sea-level (MSL) will rise by about <TT tt={['<b>7m</b>', '23 feet']} />.</span
	>
	<ul>
		<li>
			According to modelling and to historical data, there is a threshold beyond which
			self-sustained melting will continue. This threshold has been modelled to occur at a global
			mean temperature (GMT) between <TT tt={['1.7C', '3.1F']} /> and <TT tt={['2.3C', '4.1F']} /> above
			preindustrial temperatures.
		</li>
		<li>
			For several months this year (2023), we were at<TT tt={['1.5C', '2.7F']} /> above preindustrial
			temperatures so we are, potentially, very close to that tipping point.
		</li>
		<li>
			If/when we overshoot that threshold, but then manage to get GMT back to<TT
				tt={['1.5C', '2.7F']}
			/> above preindustrial temperatures, melting would slow and eventually stop. But by then MSL will
			have risen several metres.
		</li>
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
	li {
		margin-bottom: 0.5em;
	}
</style>
