<script lang="ts">
	export let num: string = `42`;
	export let leader: string = '';
	let open = false;

	function toggle() {
		open = !open;
	}
</script>

<section class="entry card p-4 flex flex-col relative">
	<button
		class="entry-toggle-button btn-icon btn-sm rounded-full bg-tertiary-400 absolute right-0 -top-3 -right-3"
		on:click={toggle}
	>
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
		<div class="slot"><slot name="content" /></div>
	{/if}
</section>

<style lang="postcss">
	.entry.card {
		@apply bg-tertiary-50;
	}
	.entry-toggle-button {
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
