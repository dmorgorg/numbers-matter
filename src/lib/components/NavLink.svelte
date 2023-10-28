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
	>{title}</a
>

<style lang="postcss">
	a {
		border-radius: 0.375rem;
		color: black;
		padding: 0.125rem 0.375rem;

		&:hover {
			color: inherit;

			&.isActive {
				@apply bg-tertiary-300;
			}

			&:not(.isActive) {
				@apply bg-tertiary-400;
			}
		}
	}
</style>
