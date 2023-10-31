<script lang="ts">
	export let tt: Array<String> = [];
</script>

<div class="trigger">
	{@html tt[0]}
	<span class="tip-text">
		{@html tt[1]}
	</span>
</div>

<style lang="postcss">
	.trigger {
		border-radius: 0.25em;
		display: inline-block;
		/* font-weight: bold; */
		padding: 0 0.125em;
		position: relative;
		/* z-index: 10; */

		&:hover {
			cursor: pointer;

			.tip-text {
				visibility: visible;
				opacity: 1;
				transform: translate(-50%, -5%) scale3d(1, 1, 1);
				transition: all 0.2s 0.1s ease-in-out;
			}
		}

		& .tip-text {
			/* background: #e0e4ec; */
			background: white;
			bottom: 115%;
			border-radius: 0.25em;
			border: 1px solid black;
			box-shadow: 0.1em 0.1em 0.1em rgba(0, 0, 0, 0.5);
			color: black;
			/* display: block; */
			font-size: 90%;
			font-weight: normal;
			left: 50%;
			line-height: 1;
			max-width: 10em;
			opacity: 0;
			padding: 0.25em;
			position: absolute;
			text-align: center;
			transform: translate(-50%, -5%) scale3d(0.1, 0.1, 1);
			transition: all 0.2s 0.1s ease-in-out;
			/* visibility: hidden; */
			width: max-content;
			/* z-index: 10; */
			text-align: center;

			&::before {
				transform: scale3d(0.2, 0.2, 1);
				transition: all 0.2s ease-in-out;
			}

			&::after {
				border-width: 0.5em;
				border-style: solid;
				border-color: black transparent transparent transparent;
				content: '';
				left: 50%;
				transform: translate3d(-50%, 0%, 0);
				transition: all 0.1s ease-in-out;
				position: absolute;
				top: 105%;
			}
		}
	}
</style>
