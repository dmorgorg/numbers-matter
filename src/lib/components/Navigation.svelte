<script lang="ts">
	import NavLink from '$lib/components/NavLink.svelte';
	let activeBackground = 'bg-tertiary-400';
</script>

<nav class="py-10 nav-component">
	<ul>
		<li>
			<NavLink href="/" title="Home" {activeBackground} />
		</li>
		<li>
			<div class="font-medium underline">
				<NavLink href="/climate" title="Climate" {activeBackground} />
			</div>
			<ul>
				<li class="font-medium">
					<NavLink href="/climate/problems" title="Problems" {activeBackground} />
					<ul>
						<li>
							<NavLink
								href="/climate/problems/pollution"
								title="<s>Pollution</s>"
								{activeBackground}
							/>
						</li>
						<li>
							<NavLink href="/climate/problems/warming" title="Warming" {activeBackground} />
						</li>
					</ul>
				</li>
				<li class="font-medium">
					<NavLink href="/climate/solutions" title="Which Solutions Work" {activeBackground} />
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
										title="Generation"
										{activeBackground}
									/>
									<ul class="subsubsection">
										<li class="font-normal">
											<NavLink
												href="/climate/solutions/electricity/generation/wind"
												title="Wind"
												{activeBackground}
											/>
										</li>
										<li class="font-normal">
											<NavLink
												href="/climate/solutions/electricity/generation/solar"
												title="Solar"
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
							<NavLink
								href="/climate/solutions/housing"
								title="<s>Housing</s>"
								{activeBackground}
							/>
						</li>
						<li>
							<NavLink
								href="/climate/solutions/industry"
								title="<s>Industry</s>"
								{activeBackground}
							/>
						</li>
					</ul>
				</li>
				<li class="font-medium">
					<NavLink
						href="/climate/notSolutions"
						title="<s>Which Don't Work (Yet)</s>"
						{activeBackground}
					/>
					<ul>
						<li>
							<NavLink href="/climate/notSolutions/ccs" title="CCS" {activeBackground} />
						</li>
					</ul>
				</li>
				<li class="font-medium">
					<NavLink href="/climate/misc" title="Miscellaneous</s>" {activeBackground} />
					<ul>
						<li>
							<NavLink href="/climate/misc/subsidies" title="Subsidies" {activeBackground} />
						</li>
					</ul>
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
