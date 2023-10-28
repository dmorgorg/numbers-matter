<script lang="ts">
	import '../app.postcss';
	import '$lib/styles/global.scss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>

<AppShell slotSidebarLeft="w-0 lg:w-64 bg-surface-500">
	<svelte:fragment slot="header">
		<AppBar background="bg-surface-500">
			<svelte:fragment slot="lead">
				<button class="lg:hidden header-button btn rounded-full bg-tertiary-400 shadow-lg">
					<span>
						<svg viewBox="0 0 100 100" class=" w-5 h-5">
							<rect width="150" height="20" />
							<rect y="40" width="150" height="20" />
							<rect y="80" width="150" height="20" />
						</svg>
					</span>
				</button>
			</svelte:fragment>
			<svelte:fragment slot="trail"
				><div
					class="header-title rounded-full font-bold text-black py-2 px-6 bg-tertiary-400 shadow-lg"
				>
					the-numbers-are-in
				</div></svelte:fragment
			>
		</AppBar>
	</svelte:fragment>
	<slot /></AppShell
>
