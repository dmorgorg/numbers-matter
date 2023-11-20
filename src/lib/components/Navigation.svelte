<script lang="ts">
	import NavLink from '$lib/components/NavLink.svelte';
	let activeBackground = 'bg-primary-400';
</script>

<nav>
	<ul>
		<li>
			<NavLink href="/" title="Home" {activeBackground} />
		</li>
		<li>
			<NavLink href="/about" title="About" {activeBackground} />
		</li>
		<li>
			<div class="font-bold underline">
				<NavLink href="/climate" title="Climate" {activeBackground} />
			</div>
			<ul>
				<li>
					<NavLink href="/climate/problems" title="Problems:" {activeBackground} />
					<ul>
						<li>
							<NavLink href="/climate/problems/pollution" title="Pollution" {activeBackground} />
						</li>
						<li>
							<NavLink href="/climate/problems/warming" title="<s>Warming</s>" {activeBackground} />
							<ul>
								<li>
									<NavLink
										href="/climate/problems/warming/causes"
										title="Causes"
										{activeBackground}
									/>
								</li>
								<li>
									<NavLink
										href="/climate/problems/warming/effects"
										title="Effects"
										{activeBackground}
									/>
								</li>
							</ul>
						</li>
					</ul>
				</li>
				<li>
					<NavLink href="/climate/solutions" title="Solutions:" {activeBackground} />
					<ul class="section">
						<li>
							<NavLink
								href="/climate/solutions/electricity"
								title="<s>Electricity</s>"
								{activeBackground}
							/>
							<ul class="subsection">
								<li>
									<NavLink
										href="/climate/solutions/electricity/generation"
										title="<s>Generation</s>"
										{activeBackground}
									/>
									<ul class="subsubsection">
										<li>
											<NavLink
												href="/climate/solutions/electricity/generation/wind"
												title="<s>Wind</s>"
												{activeBackground}
											/>
										</li>
										<li>
											<NavLink
												href="/climate/solutions/electricity/generation/solar"
												title="<s>Solar</s>"
												{activeBackground}
											/>
										</li>
									</ul>
								</li>
								<li>
									<NavLink
										href="/climate/solutions/electricity/storage"
										title="<s>Storage</s>"
										{activeBackground}
									/>
								</li>
							</ul>
						</li>
						<li>
							<NavLink
								href="/climate/solutions/transportation"
								title="<s>Transportation</s>"
								{activeBackground}
							/>
							<ul>
								<li>
									<NavLink
										href="/climate/solutions/transportation/aviation"
										title="Aviation"
										{activeBackground}
									/>
								</li>
							</ul>
						</li>
						<li>
							<NavLink href="/climate/solutions/housing" title="Housing" {activeBackground} />
						</li>
						<li>
							<NavLink href="/climate/solutions/industry" title="Industry" {activeBackground} />
						</li>
						<li>
							<NavLink href="/climate/solutions/business" title="Business" {activeBackground} />
						</li>
						<li>
							<NavLink
								href="/climate/solutions/ccs"
								title="Carbon Capture and Storage"
								{activeBackground}
							/>
							<ul>
								<li>
									<NavLink
										href="/climate/solutions/ccs/dac"
										title="Direct Air Capture"
										{activeBackground}
									/>
								</li>
							</ul>
							<!-- </li> -->
						</li>
						<li>
							<NavLink href="/climate/solutions/100pcWWS" title="100% WWS" {activeBackground} />
						</li>
					</ul>
				</li>

				<li>
					<NavLink href="/climate/misc" title="<s>Miscellaneous</s>" {activeBackground} />
					<ul>
						<li>
							<NavLink href="/climate/misc/subsidies" title="<s>Subsidies</s>" {activeBackground} />
						</li>
					</ul>
				</li>
				<li>
					<NavLink href="/climate/acronyms" title="Acronyms" {activeBackground} />
				</li>
				<li>
					<NavLink href="/climate/pick-a-value" title="Pick a value..." {activeBackground} />
				</li>
			</ul>
		</li>
		<!-- end of climate -->
	</ul>
</nav>

<!-- </div> -->

<style lang="postcss">
	ul {
		list-style: none;
		padding-left: 1.25rem;
		margin: 0;
		@apply text-primary-100;
		line-height: 1.25;
		@apply font-medium;

		&:last-child {
		}

		li {
			li {
				&::before {
					font-size: 110%;
					content: '\220e';
				}

				li {
					&::before {
						content: '>';
					}
					li {
						&::before {
							content: '\226b';
						}
						li {
							&::before {
								content: '\22d9';
							}
						}
					}
				}
			}
		}
	}
	nav {
		padding-left: 0;
		margin-left: 0;
	}
</style>
