<script lang="ts">
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';
</script>

<PageHeader>Pick a value...</PageHeader>

<section>
	<a href="/climate/solutions/css/dac#1.5C">1.5<sup>o</sup>C</a>
	<a href="/climate/problems/warming/effects#7m">7m</a>
	<a href="/climate/problems/warming/causes#11%">11%</a>
	<a href="/climate/solutions/industry#20%">20%</a>

	<a href="/climate/solutions/housing#40%">40%</a>
	<a href="/climate/solutions/100pcWWS#42.5%">42.5%</a>
	<a href="/climate/solutions/transportation/aviation#40%">54%</a>
	<a href="/climate/problems/warming/causes#57%"
		><TT tt={['57%', 'Warming attributable to aviation from contrail clouds.']} /></a
	>
	<a href="/climate/solutions/100pcWWS#57%"
		><TT tt={['57%', 'Reduction in energy demand due to transition to renewables.']} /></a
	>
	<a href="/climate/solutions/transportation/aviation#92%">92%</a>
	<a href="/climate/solutions/ccs/dac#728">728 kg/ha</a>
	<a href="/climate/solutions/industry#2000C">2000<sup>o</sup>C</a>
	<a href="/climate/solutions/ccs/dac#4000C">4000<sup>o</sup>C</a>
	<a href="/climate/solutions/100pcWWS#4.7mill">4.7 million</a>
	<a href="/climate/problems/pollution#8.7mill">8.7 million</a>
	<a href="/climate/problems/warming/causes#2bn">2bn tonnes</a>
	<a href="/climate/problems/warming/causes#546bn">54.6bn tonnes</a>
	<a href="/climate/solutions/100pcWWS#51.3trill">$51.3 trillion</a>
</section>

<style lang="postcss">
	section {
		@apply flex flex-wrap;
		@apply justify-center;
	}
	a {
		@apply bg-primary-100;
		@apply px-2 py-1 rounded-md;
		/* @apply py-1; */
		/* &::after {
			content: ', ';
		} */
		margin-right: 0.375rem;
		margin-bottom: 0.375rem;
	}
</style>
