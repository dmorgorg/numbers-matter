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
					<NavLink href="/climate/solutions" title="Solutions" {activeBackground} />
					<ul>
						<li>
							<NavLink
								href="/climate/solutions/electricity"
								title="Electricity"
								{activeBackground}
							/>
							<ul>
								<li class="font-normal">
									<NavLink
										href="/climate/solutions/electricity/generation"
										title="Generation"
										{activeBackground}
									/>
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
			</ul>
		</li>
		<!-- end of climate -->
	</ul>
</nav>

<!-- </div> -->

<style lang="scss">
	ul {
		list-style: none;
		padding-left: 2rem;
		margin-left: 0;

		li {
			margin: 0.5em;
		}
	}
	nav {
		padding-left: 0;
		margin-left: -1rem;
	}
	.s {
		color: red;
	}
</style>
