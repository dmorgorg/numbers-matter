<script lang="ts">
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';
</script>

<PageHeader>Pick a value...</PageHeader>

<section>
	<a href="/climate/problems/warming/causes#11pc">11%</a>
	<a href="/climate/problems/warming/causes#11&22">11% and 21%</a>
	<a href="/climate/solutions/industry#20pc">20%</a>
	<a href="/climate/problems/warming/causes#32&34">32% and 34%</a>
	<a href="/climate/problems/warming/causes#36&46">36% and 46%</a>
	<a href="/climate/solutions/housing#40pc">40%</a>

	<a href="/climate/solutions/100pcWWS#42.5pc">42.5%</a>
	<a href="/climate/problems/greatDivide#45pc">45%</a>
	<a href="/climate/solutions/transportation/aviation#54pc"
		><TT tt={['54%', 'Aviation contrail avoidance']} /></a
	>
	<a href="/climate/solutions/business#54pc"><TT tt={['54%', 'Work from home savings']} /></a>
	<a href="/climate/solutions/100pcWWS#57pc"
		><TT tt={['57%', 'Reduction in energy demand due to transition to renewables.']} /></a
	>
	<a href="/climate/problems/warming/causes#57pc"
		><TT tt={['57%', 'Warming attributable to aviation from contrail clouds.']} /></a
	>
	<a href="/climate/solutions/transportation/aviation#92pc">92%</a>

	<a href="/climate/solutions/css/dac#1.5C"><TT tt={['1.5<sup>o</sup>C', '2.7<sup>o</sup>F']} /></a>
	<a href="/climate/problems/warming/effects#3.2C"
		><TT tt={['3.2<sup>o</sup>C', '5.8<sup>o</sup>F']} /></a
	>
	<a href="/climate/problems/warming/effects#7m"><TT tt={['7 metres', '23 feet']} /></a>

	<a href="/climate/problems/greatDivide#7.6"
		><TT tt={['7.6<sup>o</sup>C', '13.7<sup>o</sup>F']} /></a
	>

	<a href="/climate/solutions/ccs/dac#$100">$100/ton</a>
	<a href="/climate/solutions/ccs/dac#728"><TT tt={['728 kg/ha', '650 lb/ac']} /></a>
	<a href="/climate/solutions/industry#2000C"
		><TT tt={['2,000<sup>o</sup>C', '3,600<sup>o</sup>F']} /></a
	>
	<a href="/climate/problems/greatDivide#2640">2640</a>
	<a href="/climate/problems/greatDivide#3834">3,834</a>
	<a href="/climate/solutions/ccs/dac#4000tonnes"
		><TT tt={['4,000 tonnes', '3900 (long) tons']} /></a
	>
	<a href="/climate/problems/greatDivide#7000t">7,000 tons</a>
	<a href="/climate/problems/greatDivide#1mill">1 million</a>
	<a href="/climate/problems/greatDivide#1.3mill">1.3 million</a>
	<a href="/climate/solutions/100pcWWS#4.7mill">4.7 million</a>
	<a href="/climate/problems/pollution#8.7mill">8.7 million</a>
	<a href="/climate/problems/greatDivide#$93mill">$93 million</a>
	<a href="/climate/problems/greatDivide#$120mill">$120 million</a>
	<a href="/climate/problems/greatDivide#393mill">393 million</a>

	<a href="/climate/problems/warming/causes#2bn">2bn tonnes</a>
	<a href="/climate/problems/greatDivide#2.3bn">2.3 billion</a>
	<a href="/climate/problems/warming/causes#546bn">54.6bn tonnes</a>
	<a href="/climate/problems/greatDivide#1tn">$1 trillion</a>
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
