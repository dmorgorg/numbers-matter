<script lang="ts">
	import '../app.postcss';
	import '$lib/styles/global.scss';
	import { fade } from 'svelte/transition';
	import { AppShell, AppBar, storePopup } from '@skeletonlabs/skeleton';
	import {
		Drawer,
		initializeStores,
		getDrawerStore,
		type DrawerSettings
	} from '@skeletonlabs/skeleton';

	import Navigation from '$lib/components/Navigation.svelte';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });

	initializeStores();
	const drawerStore = getDrawerStore();
	const drawerSettings: DrawerSettings = {
		id: 'left',
		bgDrawer: 'bg-surface-500',
		bgBackdrop: 'bg-surface-200/80',
		width: 'w-5/6',
		padding: 'py-5 pl-5',
		border: 'rounded-none'
	};

	function drawerOpen(): void {
		drawerStore.open(drawerSettings);
	}
	function drawerClose(): void {
		drawerStore.close();
	}
</script>

<Drawer transitions={false}>
	<div class="relative">
		<button
			class=" drawer-button btn-icon bg-tertiary-400 absolute top-4 right-4 font-extrabold text-2xl pt-0 pb-1 px-4 rounded-full"
			on:click={drawerClose}><span>&times;</span></button
		>
		<div class="nav"><Navigation /></div>
	</div>
</Drawer>

<AppShell slotSidebarLeft="w-0 lg:w-64 bg-surface-500" class="bg-white">
	<svelte:fragment slot="header">
		<AppBar background="bg-surface-500">
			<svelte:fragment slot="lead">
				<button
					class="lg:hidden header-button btn rounded-full bg-tertiary-400 shadow-lg px-3 py-2"
					on:click={drawerOpen}
				>
					<span>
						<svg viewBox="0 0 100 100" class=" w-5 h-5">
							<rect width="150" height="20" />
							<rect y="40" width="150" height="20" />
							<rect y="80" width="150" height="20" />
						</svg>
					</span>
				</button>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<div
					class="header-title rounded-full font-bold text-black py-2 px-6 bg-tertiary-400 shadow-lg"
				>
					the-numbers-matter
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft"><Navigation /></svelte:fragment>
	<!-- page content -->
	<slot />
</AppShell>
