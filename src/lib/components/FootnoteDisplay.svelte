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
				<a href={footnote[1]}>{footnote[3]}</a>
			</div>
		{/each}
	</div>
</div>

<style lang="postcss">
	.container {
		width: 27em;
		margin: 0 auto;
		display: flex;
		justify-content: center;
		padding-top: 1em;

		.footnotes {
			display: flex;
			flex-direction: column;
			align-self: center;
			align-items: flex-start;
			@apply text-tertiary-500;
			align-items: flex-start;

			h3 {
				color: black;
				text-decoration: underline;
				margin-bottom: 0.25em;
				align-self: center;
				font-weight: bold;
			}

			.footnote {
				font-size: 80%;
				padding-left: 1.375em;
				text-indent: -1.375em;

				.desc {
					color: black;
				}

				a {
					@apply text-tertiary-500;
				}
			}
		}
	}
</style>
