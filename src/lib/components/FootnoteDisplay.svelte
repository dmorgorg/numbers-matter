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
				<span class="desc">[{index + 1}] {@html footnote[0]}</span>
				<a href={footnote[1]}>{footnote[2]}</a>
			</div>
		{/each}
	</div>
</div>

<style lang="postcss">
	.container {
		width: 25em;
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
			@apply text-tertiary-500;
			align-items: flex-start;

			h3 {
				color: black;
				text-decoration: underline;
				margin-bottom: 0.25em;
				align-self: center;
			}

			.footnote {
				font-size: 85%;
				padding-left: 2.5em;
				text-indent: -2.5em;

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
