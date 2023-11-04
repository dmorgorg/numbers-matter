<script lang="ts">
	import FootnoteDisplay from '$lib/components/FootnoteDisplay.svelte';
	export let footnotes: Array<any>;

	// first <Entry> has entry=0, etc.
	let entryIndex = footnotes.length;
	// create an array to hold the footnotes for this <Entry>
	footnotes[entryIndex] = [];

	let open = false;
	function toggle() {
		open = !open;
	}
</script>

<section class="entry card p-4 flex flex-col relative">
	<!-- {entry} -->
	<button class="entry-toggle-button bg-tertiary-400 absolute -top-2 -right-2" on:click={toggle}>
		{#if !open}
			&plus;
		{:else}
			&minus;
		{/if}</button
	>
	<header class="flex items-center flex-start">
		<span class="num text-tertiary-500 font-bold text-2xl"><slot name="num" /> </span>
		<div class="ml-4"><slot name="lead" /></div>
	</header>
	{#if open}
		<div class="slot"><slot /></div>
		<FootnoteDisplay {entryIndex} {footnotes} />
	{/if}
</section>

<style lang="postcss">
	.entry {
		margin-bottom: 1.5em;
		&.card {
			@apply bg-tertiary-50;
		}
	}
	.entry-toggle-button {
		padding-bottom: 0.1em;
		border-radius: 50%;
		height: 1.5em;
		aspect-ratio: 1;
	}
	.num {
		/* text-shadow: 0 0 0.2rem black; */
	}
	.slot {
		width: 90%;
		margin: 0 auto;
		font-size: 90%;
	}
</style>
