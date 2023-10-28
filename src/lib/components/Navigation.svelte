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
					<NavLink href="/climate/renewables" title=" Renewables" {activeBackground} />
				</li>
				<ul>
					<li class="font-medium">
						<NavLink href="/climate/renewables/wind" title=" Wind" {activeBackground} />
						<ul class="font-normal">
							<li>
								<NavLink
									href="/climate/renewables/wind/turbines"
									title=" Turbines"
									{activeBackground}
								/>
							</li>
						</ul>
					</li>
					<li class="font-medium">
						<NavLink href="/climate/renewables/water" title="Water" {activeBackground} />
					</li>
					<li class="font-medium">
						<NavLink href="/climate/renewables/solar" title="Solar" {activeBackground} />
					</li>
				</ul>
				<li class="font-medium">
					<NavLink href="/climate/fossils" title=" Fossil Fuels" {activeBackground} />
				</li>
				<li class="font-medium">
					<NavLink href="/climate/consequences" title=" Consequences" {activeBackground} />
				</li>
			</ul>
		</li>
		<li class="py-2">
			<span class="font-medium underline">
				<NavLink href="/misc" title="Misc.ell.any" {activeBackground} />
			</span>
		</li>
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
</style>
