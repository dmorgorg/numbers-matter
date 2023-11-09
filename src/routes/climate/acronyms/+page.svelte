<script lang="ts">
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
</script>

<PageHeader>Acronyms Used</PageHeader>

<div class="container">
	<dl>
		<dt>BECCS</dt>
		<dd>Bioenergy with Carbon Capture and Storage</dd>
	</dl>
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
		<dd>
			<TT
				tt={[
					'Enhanced Rock Weathering',
					'Natural rock weathering occurs over hundreds of thousands of years: rain combines with CO<sub>2</sub> in the atmosphere to form a diluted carbonic acid. When this acid falls onto rocks and soil, there is an interaction where the rock sequesters the CO<sub>2</sub>. This process reduces the amount of CO<sub>2</sub> in the atmosphere, and is thought to have played a part in maintaining CO<sub>2</sub> levels in the atmosphere over many thousands of years.<br/><br/> This is an extremely slow process which enhanced rock weathering (ERW) accelerates. Rock, typically basalt, is crushed to increase its surface area to volume ratio, speeding up the sequestration process, and spread on soil where it absorbs CO<sub>2</sub>.'
				]}
				maxWidth="x-wide"
			/>
		</dd>
	</dl>
	<dl>
		<dt>GMT</dt>
		<dd>Global Mean Temperature</dd>
	</dl>
	<dl>
		<dt>GRF</dt>
		<dd>
			<TT
				tt={[
					'Glacial Rock Flour',
					'Rock powder, caused by "grinding" between rock and glacial ice.'
				]}
				maxWidth="medium"
			/>
		</dd>
	</dl>
	<dl>
		<dt>GHG</dt>
		<dd>
			<TT
				tt={[
					'Greenhouse Gases',
					'In addition to CO<sub>2</sub>, GHG include methane and nitrous oxide. There are also fluorinated gases, in smaller quantities, but with high global warming potential (GWP) '
				]}
				maxWidth="medium"
			/>
		</dd>
	</dl>
	<dl>
		<dt>GWP</dt>
		<dd>
			<TT
				tt={[
					'Global Warming Potential',
					'GWP measures the global warming impact of different gases, relative to CO<sub>2</sub>. CO<sub>2</sub> has a GWP of 1, methane of 27-30 and nitrous oxide of 273.'
				]}
				maxWidth="medium"
			/>
		</dd>
	</dl>
	<dl>
		<dt>NZE</dt>
		<dd>Net Zero Emissions</dd>
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
		width: 90%;
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
		@apply bg-gray-200;
		border-left: 0.5em solid white;
		@apply rounded-e-full;
	}

	@media screen and (min-width: 768px) {
		.container {
			width: 80%;
			margin: 0 auto;
		}
	}
	@media screen and (min-width: 1024px) {
		.container {
			width: 70%;
			margin: 0 auto;
		}
	}
</style>
