<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar, Drawer } from '@skeletonlabs/skeleton';
	import { initializeStores, getDrawerStore } from '@skeletonlabs/skeleton';
	import hljs from 'highlight.js';
	import 'highlight.js/styles/github-dark.css';
	import { LightSwitch } from '@skeletonlabs/skeleton';

	import { TreeView, TreeViewItem, type TreeViewNode } from '@skeletonlabs/skeleton';
	import { storeHighlightJs } from '@skeletonlabs/skeleton';

	storeHighlightJs.set(hljs);

	import {
		ListBox,
		ListBoxItem,
		AppRail,
		AppRailTile,
		AppRailAnchor
	} from '@skeletonlabs/skeleton';
	let valueSingle = '0';
	let currentTile = valueSingle;
	import { Avatar } from '@skeletonlabs/skeleton';
</script>

<!-- src/routes/__layout.svelte -->

<!-- App Shell -->

<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->

		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<h1 class="h1">rugby algo</h1>

			<svelte:fragment slot="lead">
				<li>
					<a href="/"> <Avatar  src="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" /> </a>
				</li>
			</svelte:fragment>

			<svelte:fragment slot="trail"
				><a
					id="button-t-b"
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/ThomasCombettes"
					target="_blank"
					rel="noreferrer"
				>
					github
				</a>
				<LightSwitch />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<!--  Tab  Bar -->
	<svelte:fragment slot="sidebarLeft">
		<div class="tab-bar">
			<TreeView>
				<TreeViewItem href="/algos">
					Algorithmes
					<svelte:fragment slot="children">
						<TreeViewItem>
							<a href="/algos/dfs"> dfs</a>
						</TreeViewItem>
						<TreeViewItem>
							<a href="/algos/bfs"> bfs</a>
						</TreeViewItem>
					</svelte:fragment>
				</TreeViewItem>
				<TreeViewItem>
					<a href="/portfolio"> portfolio</a>
				</TreeViewItem>
			</TreeView>

			<nav>
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
		</div>
	</svelte:fragment>

	<!-- Page Route Content -->
	<slot />
</AppShell>

<style>
	.tab-bar {
		padding: 100px;
		border-color: red;
		border-width: 5px;
	}
</style>
