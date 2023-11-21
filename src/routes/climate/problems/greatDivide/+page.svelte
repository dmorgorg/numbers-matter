<script lang="ts">
	import Entry from '$lib/components/Entry.svelte';
	import PageHeader from '$lib/components/PageHeader.svelte';
	import TT from '$lib/components/ToolTip.svelte';
	import FN from '$lib/components/Footnote.svelte';

	let footnotes: Array<string> = ['hello world'];
</script>

<PageHeader>The Great (Economic) Divide</PageHeader>

<Entry {footnotes} headless={true}
	>81 billionaires have as much wealth as the poorest half of the world <FN
		{footnotes}
		desc="'Survival of the Richest'"
		accessed="20th November, 2023"
		url="https://www.oxfam.org/en/research/survival-richest"
	/>. Globally, the richest 1% emit as much carbon as the poorest two-thirds of humanity, whilst
	simultaneously being the best able to protect themselves from the consequences of global warming <FN
		{footnotes}
		desc="'Climate Equality: A planet for the 99%'"
		accessed="20th November, 2023"
		url="https://webassets.oxfamamerica.org/media/documents/cr-climate-equality-201123-en.pdf"
	/>.

	<div class="width80"><img src="/images/superyacht.png" alt="superyacht" /></div>
	<br />
	<p>
		"...Those who have done the least to cause the climate crisis are the ones who are suffering the
		most."
	</p>
</Entry>

<Entry bind:footnotes id="7.6C">
	<span slot="num"><TT tt={['7.6<sup>o</sup>C', '13.7<sup>o</sup>F']} /></span>
	<span slot="lead"
		>There is an average temperature difference of <TT
			tt={['7.6<sup>o</sup>C', '13.7<sup>o</sup>F']}
		/> between formal and informal housing, notably pavement dwelling, in India <FN
			{footnotes}
			desc="'Climate Change, Heat Waves and
            Thermal Comfort—Reflections on
            Housing Policy in India'"
			accessed="21st November, 2023"
			url="https://journals.sagepub.com/doi/pdf/10.1177/0975425320906249"
		/>.
	</span>
	<div class="width80"><img src="/images/mumbai.png" alt="mumbai formal and slum housing" /></div>
	<div class="caption">The area surrounding the Bandra Kurla complex in Mumbai.</div>
	<ul>
		<li>
			Cities are typically several degrees warmer than rural areas, and areas within cities without
			much green space are hotter still. In the US, people of color tend to reside in hotter
			neighbourhoods than Whites.
		</li>
	</ul>
</Entry>
<Entry bind:footnotes id="2640">
	<span slot="num">2640</span>
	<span slot="lead"
		>There are 2640 billionaires, worth a total of $12.2 trillion, on the 2023 Forbes list <FN
			{footnotes}
			desc="'The World's Billionaires'"
			accessed="21st November, 2023"
			url="https://www.forbes.com/sites/chasewithorn/2023/04/04/forbes-37th-annual-worlds-billionaires-list-facts-and-figures-2023/?sh=12dfa68a77d7"
		/>.
	</span>
</Entry>
<Entry bind:footnotes id="1mill">
	<span slot="num">1 million</span>
	<span slot="lead"
		>Annual global emissions by the super-rice 1% cancel out the carbon savings from almost one
		million onshore wind turbines. <FN
			{footnotes}
			desc="'Climate Equality: A planet for the 99%'"
			accessed="20th November, 2023"
			url="https://webassets.oxfamamerica.org/media/documents/cr-climate-equality-201123-en.pdf"
		/>.
	</span>
</Entry>
<Entry bind:footnotes id="1.3mill">
	<span slot="num">1.3 million</span>
	<span slot="lead"
		>The emissions of the top 1%, in 2019, are enough to cause 1.3 million heat-related deaths <FN
			{footnotes}
			desc="'Richest 1% emit as much planet-heating pollution as two-thirds of humanity'"
			accessed="20th November, 2023"
			url="https://www.oxfam.org/en/press-releases/richest-1-emit-much-planet-heating-pollution-two-thirds-humanity"
		/>.
	</span>
	<ul>
		<li>The majority of these deaths will (or did) occur between 2020 and 2030.</li>
		<li>
			“The super-rich are plundering and polluting the planet to the point of destruction, leaving
			humanity choking on extreme heat, floods and drought,” said Oxfam International interim
			Executive Director Amitabh Behar.“For years we’ve fought to end the era of fossil fuels to
			save millions of lives and our planet. It’s clearer than ever this will be impossible until
			we, too, end the era of extreme wealth.”
		</li>
	</ul>
</Entry>
<Entry bind:footnotes id="$93mill">
	<span slot="num">$93 million</span>
	<span slot="lead"
		>Members of the US congress own an estimated $93 million in fossil fuel industry stocks <FN
			{footnotes}
			desc="'Members of Congress Own Up to $93 Million in Fossil Fuel
            Stocks'"
			accessed="20th November, 2023"
			url="https://prospect.org/power/members-of-congress-own-up-to-93-million-in-fossil-fuel-stocks/"
		/>.
		<!-- 70% of industrial carbon emissions since 1998 come from only 100 oil, coal and gas producers <FN
			{footnotes}
			desc="'Carbon Majors Report 2017'"
			accessed="20th November, 2023"
			url="https://cdn.cdp.net/cdp-production/cms/reports/documents/000/002/327/original/Carbon-Majors-Report-2017.pdf?1501833772"
		/>.  -->
		The 11 largest economies in the Global North provided the equivalent of US$1.8 trillion in direct
		and indirect (those relating to environmental costs) fossil fuel subsidies <FN
			{footnotes}
			desc="'Climatge Equality: A planet for the 99%'"
			accessed="20th November, 2023"
			url="https://webassets.oxfamamerica.org/media/documents/cr-climate-equality-201123-en.pdf"
		/>, or $5.9 trillion globally, in 2020 <FN
			{footnotes}
			desc="'Still Not Getting Energy Prices Right: A Global and Country Update of Fossil Fuel Subsidies'"
			accessed="20th November, 2023"
			url="https://www.imf.org/en/Publications/WP/Issues/2021/09/23/Still-Not-Getting-Energy-Prices-Right-A-Global-and-Country-Update-of-Fossil-Fuel-Subsidies-466004"
		/>.
	</span>
</Entry>
<Entry bind:footnotes id="$120mill">
	<span slot="num">$120 million</span>
	<span slot="lead"
		>Jezz Bezos announces (21st November, 2023) that he has donated almost $120 million dollars to
		help US families experiencing homelessness <FN
			{footnotes}
			desc="'Jeff Bezos Announces He’s Donated Nearly $120 Million To Help Families Experiencing Homelessness'"
			accessed="21st November, 2023"
			url="https://www.forbes.com/sites/phoebeliu/2023/11/21/jeff-bezos-announces-hes-donated-nearly-120-million-to-help-families-experiencing-homelessness/?sh=73957bad1c89"
		/>.
	</span>
	<div class="width80">
		<img src="/images/bezos.webp" alt="jeff bezos" />
		<div class="caption">
			“It’s a privilege to support these orgs in their inspiring mission to help families regain
			stability,” writes Bezos.
		</div>
	</div>
	<ul>
		<li>
			The average salary for an Amazon warehouse worker is $16.73/hour <FN
				{footnotes}
				desc="'Amazon.com salaries: How much does Amazon.com pay?'"
				accessed="21st November, 2023"
				url="https://www.indeed.com/cmp/Amazon.com/salaries"
			/>, 18% less than the $20.40 wage required for an average one-bedroom rental <FN
				{footnotes}
				desc="'Out of Reach'"
				accessed="21st November, 2023"
				url="https://nlihc.org/oor"
			/>.
		</li>
		<!-- <li>$120 million is less than a quarter of what Bezos spent on his superyacht.</li> -->
	</ul>
</Entry>
<Entry bind:footnotes id="393mill">
	<span slot="num">393 million</span>
	<span slot="lead"
		>The investments of 125 billionaires emit 393 million tons of CO<sub>2</sub> each year. As much
		as the whole of France.
		<FN
			{footnotes}
			desc="'Richest 1% emit as much planet-heating pollution as two-thirds of humanity'"
			accessed="20th November, 2023"
			url="https://www.oxfam.org/en/press-releases/richest-1-emit-much-planet-heating-pollution-two-thirds-humanity"
		/>.
	</span>
</Entry>

<Entry bind:footnotes id="2.3bn">
	<span slot="num">2.3 billion</span>
	<span slot="lead"
		>675 million people do not have access to electricity, and up to 2.3 billion people still use
		polluting fuels and technologies for cooking, largely in sub-Saharan Africa and Asia, causing
		3.2 million deaths annually <FN
			{footnotes}
			desc="'Climate Equality: A planet for the 99%'"
			accessed="21st November, 2023"
			url="https://webassets.oxfamamerica.org/media/documents/cr-climate-equality-201123-en.pdf"
		/>.
	</span>
</Entry>

<style>
	img {
		border: 1px solid black;
	}
</style>
