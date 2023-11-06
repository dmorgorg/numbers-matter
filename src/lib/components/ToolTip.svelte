<script lang="ts">
	export let tt: Array<String> = [];
	export let maxWidth: string = 'normal';
</script>

<div class="trigger">
	{@html tt[0]}
	<span
		class="tip-text"
		class:normal={maxWidth == 'normal'}
		class:medium={maxWidth == 'medium'}
		class:wide={maxWidth == 'wide'}
		class:x-wide={maxWidth == 'x-wide'}
	>
		{@html tt[1]}
	</span>
</div>

<style lang="postcss">
	.trigger {
		border-radius: 0.25em;
		display: inline-block;
		font-weight: 500;
		padding: 0 0.125em;
		position: relative;
		/* z-index: 10; */

		&:hover {
			cursor: pointer;

			.tip-text {
				visibility: visible;
				opacity: 1;
				transform: translate(-50%, 0) scale3d(1, 1, 1);
				transition: all 0.6s 0.1s ease-in-out;
			}
		}

		& .tip-text {
			background: white;
			bottom: 2.25em;
			border-radius: 0.25em;
			border: 1px solid black;
			box-shadow: 0.1em 0.1em 0.1em rgba(0, 0, 0, 0.5);
			color: black;
			font-size: 90%;
			font-weight: normal;
			left: 45%;
			line-height: 1;
			/* max-width: 10em; */
			opacity: 0;
			padding: 0.5em;
			padding-bottom: 0.75em;
			position: absolute;
			text-align: center;
			transform: translate(-55%, 0) scale3d(0.1, 0.1, 1);
			transition: all 0.7s 0.1s ease-in-out;
			width: max-content;
			/* z-index: 10000000; */

			&.normal {
				max-width: 10em;
			}
			&.medium {
				max-width: 17.5em;
			}
			&.wide {
				max-width: 22.5em;
			}
			&.x-wide {
				max-width: 60ch;
			}

			&::before {
				transform: scale3d(0.2, 0.2, 1);
				transition: all 5s ease-in-out;
			}

			&::after {
				border-width: 0.75em;
				border-style: solid;
				border-color: black transparent transparent transparent;
				content: '';
				left: 50%;
				/* transform: translate3d(-50%, 0%, 0); */
				transition: all 1s ease-in-out;
				position: absolute;
				top: 100%;
			}
		}
	}

	@media screen and (max-width: 480px) {
		.trigger .tip-text.x-wide {
			max-width: 50ch;
			left: 35%;
		}
	}
</style>
