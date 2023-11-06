<script lang="ts">
	import FootnoteDisplay from '$lib/components/FootnoteDisplay.svelte';
	export let footnotes: Array<any>; // to enlarge font
	export let headless: boolean = false;
	let open: boolean = false;
	$: blank = false;

	// first <Entry> has entry=0, etc.
	let entryIndex: number = footnotes.length;
	// create an array to hold the footnotes for this <Entry>
	footnotes[entryIndex] = [];

	if (headless) {
		open = true;
	}
	$: if (headless && !open) {
		blank = true;
	}

	function toggle() {
		open = !open;
	}
</script>

<div class="relative pb-2 pt-2">
	<button class="entry-toggle-button bg-tertiary-500 absolute -top-1 -right-2" on:click={toggle}>
		{#if !open}
			<b>&plus;</b>
		{:else}
			<b>&minus;</b>
		{/if}</button
	>
	<section class="entry card flex flex-col p-4" class:blank class:headless>
		<header class="flex items-center flex-start">
			<span class="num text-tertiary-600 font-bold text-2xl"><slot name="num" /> </span>
			<div class="ml-4"><slot name="lead" /></div>
		</header>

		<div class="slot pt-2" class:hide={!open} class:headless>
			<slot />
			<FootnoteDisplay {entryIndex} {footnotes} />
		</div>
	</section>
</div>

<style lang="postcss">
	section {
		border-color: #598792;
		@apply border-s-8;
	}
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
	.hide {
		display: none;
	}
	.headless {
		font-size: 100%;
	}
	.blank {
		padding: 0;
	}
</style>
