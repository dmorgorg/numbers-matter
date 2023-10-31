<script>
	let link =
		'https://www.nature.com/articles/s41586-023-06503-9.epdf?sharing_token=uM50_RcUz4zkGFgBOXzH8NRgN0jAjWel9jnR3ZoTv0PT1p_hQwiMqEqpCXKZLjNJlG-pthmBWCBxpbig2NOfwIeHOplJDOSnt9Vt9OHSYM9wOSg80by7OHvNJIOKbz9JZdMjyxmZ1ticBjCJj8jaT7rduXaM4ajLaxus0ykIO1Y%3D';
	let truncated = link.slice(0, 40) + ' . . .';
	// truncated = link;
</script>

<p>link: {link}</p>
<br />
<p>trunc: {truncated}</p>

<div class="container">
	<div class="footnotes">
		<div class="footnote">
			this is a footnote this this is a footnote this is a footnote: <a href={link}>{truncated}</a>
		</div>

		<div class="footnote">
			this is a footnote
			<a href={link}>{truncated}</a>
		</div>
		<div class="footnote">
			this is a footnote
			<a href={link}>{truncated}</a>
		</div>
	</div>
</div>

<style lang="postcss">
	.container {
		width: 80%;
		margin: 0 auto;
		display: flex;
		flex-direction: column;
		align-items: center;
		border: 1px solid green;

		.footnotes {
			display: flex;
			flex-direction: column;
			align-items: flex-start;
			color: red;

			.footnote {
				font-size: 85%;
				display: inline;
				margin-top: 0.5em;
				padding-left: 1.5em;
				text-indent: -1.5em;
			}
		}
	}
</style>
