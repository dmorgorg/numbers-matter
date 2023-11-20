<script lang="ts">
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';
</script>

<PageHeader>Pick a value...</PageHeader>

<section>
	<a href="/climate/solutions/css/dac#1.5C"><TT tt={['1.5<sup>o</sup>C', '2.7<sup>o</sup>F']} /></a>
	<a href="/climate/problems/warming/effects#3.2C"
		><TT tt={['3.2<sup>o</sup>C', '5.8<sup>o</sup>F']} /></a
	>
	<a href="/climate/problems/warming/effects#7m">7 metres</a>
	<a href="/climate/problems/warming/causes#11%">11%</a>
	<a href="/climate/problems/warming/causes#11&22">11% and 21%</a>
	<a href="/climate/solutions/industry#20%">20%</a>
	<a href="/climate/problems/warming/causes#32&34">32% and 34%</a>
	<a href="/climate/problems/warming/causes#36&46">36% and 46%</a>
	<a href="/climate/solutions/housing#40%">40%</a>
	<a href="/climate/solutions/100pcWWS#42.5%">42.5%</a>
	<a href="/climate/solutions/transportation/aviation#54%"
		><TT tt={['54%', 'Aviation contrail avoidance']} /></a
	>
	<a href="/climate/solutions/solutions/business#40%"
		><TT tt={['54%', 'Work from home savings']} /></a
	>
	<a href="/climate/problems/warming/causes#57%"
		><TT tt={['57%', 'Warming attributable to aviation from contrail clouds.']} /></a
	>
	<a href="/climate/solutions/100pcWWS#57%"
		><TT tt={['57%', 'Reduction in energy demand due to transition to renewables.']} /></a
	>
	<a href="/climate/solutions/transportation/aviation#92%">92%</a>
	<a href="/climate/solutions/ccs/dac#$100">$100/ton</a>
	<a href="/climate/solutions/ccs/dac#728">728 kg/ha</a>
	<a href="/climate/solutions/industry#2000C">2000<sup>o</sup>C</a>
	<a href="/climate/solutions/ccs/dac#4000C">4000<sup>o</sup>C</a>
	<a href="/climate/problems/greatDivide#1mill">1 million</a>
	<a href="/climate/problems/greatDivide#1.3mill">1.3 million</a>
	<a href="/climate/solutions/100pcWWS#4.7mill">4.7 million</a>
	<a href="/climate/problems/pollution#8.7mill">8.7 million</a>
	<a href="/climate/problems/greatDivide#$93mill">$93 million</a>
	<a href="/climate/problems/greatDivide#$393mill">$393 million</a>
	<a href="/climate/problems/warming/causes#2bn">2bn tonnes</a>
	<a href="/climate/problems/greatDivide#2.3bn">2.3 billion</a>
	<a href="/climate/problems/warming/causes#546bn">54.6bn tonnes</a>
	<a href="/climate/solutions/100pcWWS#51.3trill">$51.3 trillion</a>
</section>

<style lang="postcss">
	section {
		@apply flex flex-wrap;
		@apply justify-center;
	}
	a {
		@apply bg-primary-200;
		@apply px-2 py-1 rounded-md;
		@apply border;
		border-color: #568056;
		border-color: #89a689;

		margin-right: 0.375rem;
		margin-bottom: 0.375rem;

		&:hover {
			@apply bg-primary-50;
			@apply shadow-sm shadow-black;
			@apply border-black;
		}
	}
</style>
