<script lang="ts">
	import NavLink from '$lib/components/NavLink.svelte';
	import NavLink2 from '$lib/components/NavLink2.svelte';
	import TT from './ToolTip.svelte';
	let activeBackground = 'bg-tertiary-400';
</script>

<nav class="py-10 nav-component">
	<ul>
		<li>
			<NavLink href="/" title="Home" {activeBackground} />
		</li>
		<li>
			<NavLink href="/about" title="About" {activeBackground} />
		</li>
		<li>
			<div class="font-medium underline">
				<NavLink href="/climate" title="Climate" {activeBackground} />
			</div>
			<ul>
				<li class="font-medium">
					<NavLink href="/climate/problems" title="Problems:" {activeBackground} />
					<ul>
						<li>
							<NavLink
								href="/climate/problems/pollution"
								title="<s>Pollution</s>"
								{activeBackground}
							/>
						</li>
						<li>
							<NavLink href="/climate/problems/warming" title="<s>Warming</s>" {activeBackground} />
							<ul>
								<li class="font-normal">
									<NavLink
										href="/climate/problems/warming/causes"
										title="Causes"
										{activeBackground}
									/>
								</li>
								<li class="font-normal">
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
				<li class="font-medium">
					<NavLink href="/climate/solutions" title="Solutions:" {activeBackground} />
					<ul class="section">
						<li>
							<NavLink
								href="/climate/solutions/electricity"
								title="Electricity"
								{activeBackground}
							/>
							<ul class="subsection">
								<li class="font-normal">
									<NavLink
										href="/climate/solutions/electricity/generation"
										title="<s>Generation</s>"
										{activeBackground}
									/>
									<ul class="subsubsection">
										<li class="font-normal">
											<NavLink
												href="/climate/solutions/electricity/generation/wind"
												title="<s>Wind</s>"
												{activeBackground}
											/>
										</li>
										<li class="font-normal">
											<NavLink
												href="/climate/solutions/electricity/generation/solar"
												title="<s>Solar</s>"
												{activeBackground}
											/>
										</li>
									</ul>
								</li>
								<li class="font-normal">
									<NavLink
										href="/climate/solutions/electricity/storage"
										title="Storage"
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
						</li>
						<li>
							<NavLink href="/climate/solutions/housing" title="Housing" {activeBackground} />
						</li>
						<li>
							<NavLink href="/climate/solutions/industry" title="Industry" {activeBackground} />
						</li>
						<li>
							<NavLink2 href="/climate/solutions/ccs" {activeBackground}
								><TT tt={['CCS', 'Carbon Capture and Storage']} /></NavLink2
							>
							<ul>
								<li class="font-normal">
									<NavLink2 href="/climate/solutions/ccs/dac" {activeBackground}
										><TT tt={['DAC', 'Direct Air Capture']} />
									</NavLink2>
								</li>
							</ul>
							<!-- </li> -->
						</li>
					</ul>
				</li>

				<li class="font-medium">
					<NavLink href="/climate/misc" title="<s>Miscellaneous</s>" {activeBackground} />
					<ul>
						<li>
							<NavLink href="/climate/misc/subsidies" title="<s>Subsidies</s>" {activeBackground} />
						</li>
					</ul>
				</li>
				<li class="font-medium">
					<NavLink href="/climate/acronyms" title="Acronyms Explained" {activeBackground} />
				</li>
			</ul>
		</li>
		<!-- end of climate -->
	</ul>
</nav>

<!-- </div> -->

<style lang="scss">
	ul {
		list-style: none;
		padding-left: 1.25rem;
		margin-left: 0;
		margin-top: 0.25em;

		li {
			margin: 0.125em;
			margin: 0;
		}
	}
	nav {
		padding-left: 0;
		margin-left: 0;
	}
</style>
