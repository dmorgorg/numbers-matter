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
		class="page-header rounded-full font-bold text-black py-2 px-6 bg-tertiary-400 shadow-xl my-6 text-xl"
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
</style>
