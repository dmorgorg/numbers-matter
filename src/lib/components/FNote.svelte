<script lang="ts">
	export let desc: string;
	export let href;
	export let chars = 60;
	let truncated = href.slice(0, chars);
	if (truncated.length < href.length) {
		truncated += ' . . .';
	}

	// let index = footnotes.length;
	// footnotes[index] = [desc, href, truncated];
</script>

<span>[{3 + 1}]</span>
<br />{desc}
<br />{truncated}

<style lang="postcss">
	span {
		/* cursor: pointer; */
		@apply text-tertiary-500;
	}
</style>
