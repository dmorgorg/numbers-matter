<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>Effects of Global Warming</PageHeader>

<Entry bind:footnotes id="7m">
	<span slot="num"><TT tt={['7m', '23 feet']} /></span>
	<span slot="lead"
		>The Greenland ice sheet is melting. At our current rate of increasing carbon emissions, we are
		on track for it all to disappear. If that happens, mean sea-level (MSL) will rise by about <TT
			tt={['<b>7m</b>', '23 feet']}
		/> (due to the Greenland ice sheet alone).</span
	>
	<!-- <img src="/images/g78.jpg" alt="first ascent of a nunatak in eastern Greenland, 1969" /> -->
	<ul>
		<li>
			According to modelling and to historical data, there is a threshold beyond which
			self-sustained melting will continue. This threshold has been modelled to occur at a global
			mean temperature (GMT) between <TT tt={['1.7C', '3.1F']} /> and <TT tt={['2.3C', '4.1F']} /> above
			preindustrial temperatures. <FN
				{footnotes}
				desc="'Overshooting the critical threshold for the Greenland ice sheet.'"
				url="https://www.nature.com/articles/s41586-023-06503-9.epdf?sharing_token=uM50_RcUz4zkGFgBOXzH8NRgN0jAjWel9jnR3ZoTv0PT1p_hQwiMqEqpCXKZLjNJlG-pthmBWCBxpbig2NOfwIeHOplJDOSnt9Vt9OHSYM9wOSg80by7OHvNJIOKbz9JZdMjyxmZ1ticBjCJj8jaT7rduXaM4ajLaxus0ykIO1Y%3D"
			/>
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
			If GMT rises enough for the Greenland ice sheet to melt, then we shall have to contend with
			the extra sea-level rise (SLR) due to melting occurring in Antarctica.
		</li>

		<li>
			Greenland's ice sheet produces 1 billion (1x10<sup>9</sup>) tonnes of 'rock flour' each year
			which could be utilised for (limited) carbon capture. <FN
				{footnotes}
				url="https://www.numbers-matter.org/climate/solutions/ccs/dac"
				desc="A page within this site:"
			/>
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
	/* .container {
		width: 80%;
		margin: 0 auto;
		display: flex;
		justify-content: center;
		padding-top: 1em;

		.footnotes {
			display: flex;
			flex-direction: column;
			align-self: center;
			align-items: flex-start;
			/* font-size: 80%; */
	/* @apply text-tertiary-500;
			align-items: flex-start;

			h1 {
				color: black;
				text-decoration: underline;
				margin-bottom: 0.25em;
				align-self: center;
			}

			.footnote {
				font-size: 85%;
				padding-left: 2.5em;
				text-indent: -2.5em;
			}
		}
	} */
</style>
