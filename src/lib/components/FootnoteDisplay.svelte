<script lang="ts">
	export let entryIndex: number;
	export let footnotes: Array<any>;
</script>

<div class="container">
	<div class="footnotes">
		{#if footnotes[entryIndex].length === 1}
			<h3>Reference:</h3>
		{:else if footnotes[entryIndex].length > 1}
			<h3>References:</h3>
		{/if}
		{#each footnotes[entryIndex] as footnote, index}
			<div class="footnote">
				<span class="desc"
					>[{index + 1}] {@html footnote[0]}
					{#if footnote[2].length > 0}
						<nobr>(Accessed on {@html footnote[2]})</nobr>
					{/if}
				</span>
				<nobr><a href={footnote[1]}>{footnote[3]}</a></nobr>
			</div>
		{/each}
	</div>
</div>

<style lang="postcss">
	.container {
		width: 27em;
		/* border: 1px solid black; */
		max-width: 100%;
		margin: 0 auto;
		display: flex;
		justify-content: center;
		padding-top: 1em;

		.footnotes {
			display: flex;
			flex-direction: column;
			align-self: center;
			align-items: flex-start;
			@apply text-primary-500;
			align-items: flex-start;
			overflow-x: hidden;

			h3 {
				color: black;
				text-decoration: underline;
				margin-bottom: 0.25em;
				align-self: center;
				text-align: center;
				font-weight: bold;
			}

			.footnote {
				font-size: 80%;
				padding-left: 1.375em;
				text-indent: -1.375em;
				/* overflow-x: hidden; */
				/* border: 1px solid black; */

				.desc {
					color: black;
				}

				a {
					@apply text-primary-500;

					&:hover {
						text-decoration: underline;
					}
				}
			}
		}
	}
</style>
