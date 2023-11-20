<script lang="ts">
	import { page } from '$app/stores';
	export let title: string;
	export let href: string;
	export let activeBackground: string;

	import { getDrawerStore } from '@skeletonlabs/skeleton';
	const drawerStore = getDrawerStore();

	function drawerClose(): void {
		drawerStore.close();
	}
	// export let hoverBackground: string;
	$: active = (href: string) => (href === $page.url.pathname ? `${activeBackground}` : '');
</script>

<a {href} class={active(href)} class:isActive={active(href) !== ''} on:click={drawerClose}
	>{@html title}</a
>

<style lang="postcss">
	a {
		border-radius: 0.375em;
		@apply text-primary-100;
		padding: 0 0.175em 0.15em 0.175em;
		margin-left: 0.25em;

		&.isActive {
			box-shadow: 0.1em 0.1em 0.5em 0.025em rgb(0 0 0 / 0.25);
			@apply text-black;
			@apply bg-primary-300;
		}

		&:hover {
			box-shadow: 0.1em 0.1em 0.5em 0.025em rgb(0 0 0 / 0.125);
			@apply text-black;

			/* &.isActive {
				@apply bg-primary-200;
			} */

			&:not(.isActive) {
				@apply bg-primary-400;
			}
		}
	}
</style>
