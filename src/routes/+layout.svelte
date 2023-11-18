<script lang="ts">
	import '../app.postcss';
	import '$lib/styles/global.scss';
	// import { fade } from 'svelte/transition';
	import { AppShell, AppBar, storePopup } from '@skeletonlabs/skeleton';
	import {
		Drawer,
		initializeStores,
		getDrawerStore,
		type DrawerSettings
	} from '@skeletonlabs/skeleton';

	import Navigation from '$lib/components/Navigation.svelte';

	$: slotSidebarLeft = $page.url.pathname === '/' ? 'w-0' : 'lg:w-auto bg-tertiary-600 pr-4';

	// Floating UI for Popups
	// import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { page } from '$app/stores';
	// storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });

	initializeStores();
	const drawerStore = getDrawerStore();
	const drawerSettings: DrawerSettings = {
		id: 'left',
		bgDrawer: 'bg-tertiary-700',
		bgBackdrop: 'bg-surface-200/80',
		width: 'w-auto',
		// padding: 'py-2 pl-2',
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
			class=" drawer-button btn-icon bg-tertiary-300 absolute top-4 right-4 font-extrabold text-2xl pt-0 pb-1 px-4 rounded-full text-black"
			on:click={drawerClose}><span>&times;</span></button
		>
		<div class="nav"><Navigation /></div>
	</div>
</Drawer>

<AppShell {slotSidebarLeft} class="bg-white">
	<!-- <AppShell slotSidebarLeft="w-0 lg:w-auto bg-tertiary-600 pr-4 pt-0" class="bg-white"> -->
	<svelte:fragment slot="header">
		<AppBar background="bg-tertiary-600 z-0">
			<svelte:fragment slot="lead">
				<button
					class="lg:hidden header-button btn rounded-full bg-tertiary-300 shadow-lg px-5 py-3 drawer-button"
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
					class="site-title rounded-full font-bold text-tertiary-700 py-2 px-6 bg-tertiary-300 shadow-lg text-xl"
				>
					numbers-matter
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft"
		><div class="sidebar pr-2"><Navigation /></div></svelte:fragment
	>
	<!-- page content -->
	<div class="p-2"><slot /></div>
</AppShell>
