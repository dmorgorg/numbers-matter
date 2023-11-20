<script type>
	export let justify = 'center';
</script>

<header
	class="flex"
	class:center={justify == 'center'}
	class:left={justify == 'left'}
	class:right={justify == 'right'}
>
	<div
		class="page-header rounded-full font-bold text-primary-50 py-2 px-6 bg-primary-500 shadow-xl my-6 text-xl border border-black"
	>
		<slot />
	</div>
</header>

<style>
	.center {
		justify-content: center;
	}
	.left {
		justify-content: flex-start;
	}
	.right {
		justify-content: flex-end;
	}
	/* .page-header {
		box-shadow: 0.05em 0.05em 0.15em rgb(0 0 0 / 0.25);
	} */
</style>
