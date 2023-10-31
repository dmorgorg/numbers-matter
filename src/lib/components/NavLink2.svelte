<script lang="ts">
	import { page } from '$app/stores';
	// export let title: string;
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
	><slot /></a
>

<style lang="postcss">
	a {
		border-radius: 0.375em;
		color: black;
		padding: 0.025em 0.375em 0.0625em 0.375em;
		padding: 0 0.375em;

		&.isActive {
			box-shadow: 0.1em 0.1em 0.5em 0.025em rgb(0 0 0 / 0.25);
		}

		&:hover {
			box-shadow: 0.1em 0.1em 0.5em 0.025em rgb(0 0 0 / 0.125);

			&.isActive {
				@apply bg-tertiary-300;
			}

			&:not(.isActive) {
				@apply bg-tertiary-400;
			}
		}
	}
</style>
