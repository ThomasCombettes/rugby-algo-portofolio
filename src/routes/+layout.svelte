<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar, Drawer } from '@skeletonlabs/skeleton';
	import { initializeStores, getDrawerStore } from '@skeletonlabs/skeleton';

	import { ListBox, ListBoxItem , AppRail, AppRailTile, AppRailAnchor} from '@skeletonlabs/skeleton';
			let valueSingle = "0"
			let currentTile = valueSingle;
</script>
<!-- src/routes/__layout.svelte -->


<!-- App Shell -->

<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->

		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
				<button class="lg:hidden btn btn-sm mr-4">
					<strong class="text-xl uppercase">Menu</strong>
				</button>
			</svelte:fragment>

			<h1 class="h1">
				<span
					class="bg-gradient-to-br from-pink-500 to-violet-500 bg-clip-text text-transparent box-decoration-clone"
					>rugby</span
				>
				<span
					class="bg-gradient-to-br from-red-500 to-yellow-500 bg-clip-text text-transparent box-decoration-clone"
					>algo</span
				>
			</h1>
			<svelte:fragment slot="trail"
				><a
					id="button-t-b"
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/ThomasCombettes"
					target="_blank"
					rel="noreferrer"
				>
					github
				</a></svelte:fragment
			>
		</AppBar>
	</svelte:fragment>

	<!--  Tab  Bar -->
	<svelte:fragment slot="sidebarLeft">	
		<nav>
			<li>
				<p> ------------------------------------- </p>
			</li>
			<li>
				<a href="/"> home </a>
			</li>
			<li>
				<a href="/algos/dfs"> dfs</a>
			</li>
			<li>
				<a href="/algos/bfs"> bfs</a>
			</li>
		</nav>

	</svelte:fragment>


	
	<!-- Page Route Content -->
	<slot />
</AppShell>
