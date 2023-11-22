<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Electricity Storage</PageHeader>

<Entry bind:footnotes id="151kWh">
	<span slot="num">$151/kWh</span>
	<span slot="lead"
		>Between 2016 and 2022, lithium-ion battery packs more than halved in price, down to $151 per
		kilowatt hour <FN
			{footnotes}
			desc="'Top 10 Energy Storage Trends in 2023'"
			accessed="22nd November, 2023"
			url="https://about.bnef.com/blog/top-10-energy-storage-trends-in-2023/"
		/>. 68 gas plant projects have been cancelled, or paused, as giant batteries that can ensure
		stable power supply and protect against wind and solar variability become cheaper <FN
			{footnotes}
			desc="'Giant batteries drain economics of gas power plants'"
			accessed="22nd November, 2023"
			url="https://www.reuters.com/business/energy/giant-batteries-drain-economics-gas-power-plants-2023-11-21/"
		/>.
	</span>

	<img src="/images/batteryPrices.png" alt="battery price chart" />

	<ul>
		<li>
			The economics of those gas-fired plants used primarily to compensate for the intermittance of
			renewables are changing as back up battery power becomes competitive. Financing is harder to
			get for new gas-fired plant because of uncertainty over revenues as they no longer need to run
			continuously.
		</li>
	</ul>
</Entry>

<style>
	img {
		border: 2px solid black;
	}
</style>
