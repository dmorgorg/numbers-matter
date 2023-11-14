<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = [];
</script>

<PageHeader>Solutions for Industry</PageHeader>

<Entry {footnotes} headless={true}>
	In the US, industry is responsible for <strong>28%</strong> of CO<sub>2</sub> emissions <FN
		{footnotes}
		desc="'U.S. CO<sub>2</sub> emissions from energy consumption by source and sector, 2022'"
		url="https://www.eia.gov/energyexplained/energy-and-the-environment/where-greenhouse-gases-come-from.php"
	/>. It relies heavily on natural gas, petroleum and electricity generated using fossil fuels. But
	most industrial processes cannot be shut down when the sun sets or the wind doesn't blow. Also,
	heavy plant must often run continuously for economic reasons due to the large investments
	involved. The intermittency, or variability, of renewable power sources such as wind and solar
	make decarbonizing industry a big challenge.
</Entry>

<Entry {footnotes}>
	<span slot="num">1/5</span>
	<span slot="lead"
		>Industrial heat makes up one-fifth of global energy consumption, mostly originating from fossil
		fuel combustion<FN
			{footnotes}
			desc="'Clean and efficient heat for industry'"
			url="https://www.iea.org/commentaries/clean-and-efficient-heat-for-industry"
		/>. Due to increasing demand, the production of industrial heat is expected to account for
		one-quarter of global emissions by 2040.
	</span>
	<ul>
		<li>
			Industrial heat is often generated on site, tailored to the industrial process' particular
			needs. Cement kilns require higher temperatures than washing and drying applications in the
			food industry. A heat-pump cannot replace a gas-boiler where high temperature heat is
			required.
		</li>
		<li>
			Substituting gas for coal provides benefit but is inconsistent with reaching climate targets
			that require the world to become net-zero.
		</li>
		<li>
			Proposed solutions include the electrification of thermal processes for heating solid
			materials, steam generation and fluid heating. Using clean hydrogen as a fuel is also
			applicable to all industrial thermal processes <FN
				{footnotes}
				desc="'Thermal Process Intensification: Transforming the Way
            Industry Uses Thermal Process Energy'"
				url="https://www.energy.gov/sites/default/files/2022-05/TPI%20Workshop%20Report_AMO.pdf"
			/>. The advent of thermal batteries is also an exciting development that shows much promise.
		</li>
		<li>
			Some decarbonisation may be realised by carbon capture of flue gases but this generally needs
			significant power input; in the end, not much benefit is gained unless the electricity is
			generated from renewables.
		</li>
	</ul>
</Entry>

<Entry {footnotes}>
	<span slot="num"><TT tt={['2000<sup>o</sup>C', '3600<sup>o</sup>F']} /></span>
	<span slot="lead"
		>A thermal battery developed by Antora Energy<FN
			{footnotes}
			desc="Antora Energy"
			url="https://antoraenergy.com/"
		/> stores heat over a temperature of <TT tt={['2000<sup>o</sup>C', '3600<sup>o</sup>F']} /> and can
		be used for heat-intensive production such as steel or concrete.
	</span>
	<ul>
		<li>
			<strong>This is really cool tech!</strong> Listen to the podcast! <FN
				{footnotes}
				desc="'A super-battery aimed at decarbonizing industry'"
				url="https://transcripts.volts.wtf/a-super-battery-aimed-at-decarbonizing-industry"
			/>. Details below.
		</li>
		<li>
			Batteries will be heated when renewable electricity is cheap, or negatively priced. The stored
			heat can then displace natural gas boilers and other fossil fuel heat sources.
		</li>
		<li>
			Each battery is, at its most basic, a rock in a box. The rock used is solid carbon, chosen
			because of its abundance, cost and its stability. Carbon has a special quality: it becomes
			better at storing energy as it gets hotter. It can store three times as much heat at <TT
				tt={['800<sup>o</sup>C', '1450<sup>o</sup>F']}
			/> as it can at room temperature. Graphite, a form of carbon, is used as electrodes in steel-making
			electric-arc furnaces because of its ability to withstand very high temperatures (up to <TT
				tt={['3000<sup>o</sup>C', '5400<sup>o</sup>F']}
			/>). It also gets stronger as you heat it (up to <TT
				tt={['2400<sup>o</sup>C', '4300<sup>o</sup>F']}
			/>).
		</li>
		<li>
			An electrical resistive coil heats up the graphite until it up to its glowing white operating
			temperature of <TT tt={['2000<sup>o</sup>C', '3600<sup>o</sup>F']} />. Graphite has high
			thermal conductivity so the heat moves readily from the resistive coil throughout the block
			and there are no concerns with inconsistent heating. (This property is also useful when
			retrieving the heat.)
		</li>
		<li>
			Light is used to extract the energy from the battery. The light can be used to heat up fluid
			in a pipe or to create steam, which is what typical heat batteries do. Or the light can be
			shone on photovoltaic panels to generate electricity.
		</li>
		<li>
			The battery has an insulated door that can be closed to turn off the battery or opened to
			harness the heat and light. Progressively opening the door compensates for the light that is
			slowly dimming as the battery system cools so that there is a consistent discharge.
		</li>
		<li>
			The graphite is cooler than the sun but much closer to the photovoltaic panel; the light
			reaching the panel is hundreds of times brighter than the light emitted by the sun. The
			photovoltaics are water-cooled to deal with this.
		</li>
		<li>
			With photovoltaics, not all photons are converted to electrons; they don't all have the right
			energy density. Most photons, in solar &ndash; and in Antora Energy's specially designed<TT
				tt={['TPV', 'Thermal Photovoltaic Panels']}
			/> &ndash; simply pass through the panel. In the case of solar, this is a waste. But the TPV has
			an infra-red mirror on the back of the cells that reflects the photons back to the battery where
			they are reabsorbed, increasing the efficiency of the system. Solar cells have a maximum theoretical
			efficiency of 33% and in practice conventional solar cells have an efficiency just over 20%. The
			TPV, with its reflection and reabsorption of photons, has reached 40%.
		</li>
		<li>
			A shutter in front of the photovoltaics and a separate shutter in front of something
			extracting heat means each can be independently controlled.
		</li>
	</ul>
</Entry>

<style lang="postcss">
	ul {
		list-style-type: disc;
		margin-top: 1em;
		margin-left: 2em;

		li {
			margin-bottom: 0.5em;
		}
	}
</style>
