<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar, Drawer } from '@skeletonlabs/skeleton';
	import TopBar from './appbar.svelte';
	import TabBar from './tabbar.svelte';
	import { initializeStores, getDrawerStore } from '@skeletonlabs/skeleton';
	import Tabbar from './tabbar.svelte';

	initializeStores();

	function drawerOpen() {
		drawerStore.open({});
	}

	const drawerStore = getDrawerStore();
</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->

		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
				<button class="lg:hidden btn btn-sm mr-4" on:click={drawerOpen}>
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
			<!--  
				<Drawer class="lg:hidden btn btn-sm mr-4">
					<TabBar />
				</Drawer>
				
				Tab  Bar -->
				<Tabbar />
	</svelte:fragment>

	

	<svelte:fragment slot="footer">Thomas Combettes</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
