<script lang="ts">
	export let footnotes;
	export let desc;
	export let url: string;
	export let accessed: string = '';
	export let chars = 60;
	let truncated = url.slice(0, chars);
	if (truncated.length < url.length) {
		truncated += ' . . .';
	}

	// get index for this entry
	// footnotes already has footnotes[entry] created so subtract 1 to get back to indices
	let entry = footnotes.length - 1;
	let footnoteIndex = footnotes[entry].length;
	footnotes[entry][footnoteIndex] = [desc, url, accessed, truncated];
</script>

<span> <a href={url}>[{footnoteIndex + 1}]</a></span>

<style lang="postcss">
	span {
		/* cursor: pointer; */
		@apply text-primary-500;
	}
</style>
