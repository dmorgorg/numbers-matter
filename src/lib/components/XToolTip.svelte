<script lang="ts">
	import { popup } from '@skeletonlabs/skeleton';
	import type { PopupSettings } from '@skeletonlabs/skeleton';
	export let tt: Array<String> = [];

	const popupInfo: PopupSettings = {
		event: 'hover',
		target: 'popupInfo_' + tt[0],
		placement: 'top-start'
	};
</script>

<span class="hover:bg-white px-1 py-0 bg-surface-100 rounded-md" use:popup={popupInfo}>
	{@html tt[0]}
</span>
<!-- <div class="tip px-5 pb-0 h-sm my-0 bg-white rounded-md" data-popup="popupInfo_{tt[0]}"> -->
<div class="tip bg-white px-1 py-0 w-1/6 rounded-md" data-popup="popupInfo_{tt[0]}">
	<div class="arrow bg-white" />
	<p>{@html tt[1]}</p>
</div>

<style lang="postcss">
	.tip {
		z-index: 100;
		/* box-shadow: 0.1em 0.1em 0.5em 0.025em rgb(0 0 0 / 0.25); */
	}
	.arrow {
		box-shadow: 0.1em 0.1em 0.5em rgb(0 0 0 / 0.25);
	}
</style>
