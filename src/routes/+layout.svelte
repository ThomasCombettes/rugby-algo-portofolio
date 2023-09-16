<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import TopBar from './appbar.svelte'
	import TabBar from './tabbar.svelte';
</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<TopBar/>
	
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<TabBar />
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
