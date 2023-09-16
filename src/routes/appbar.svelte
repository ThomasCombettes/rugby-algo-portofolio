<script>
	import { AppShell, AppBar, Avatar } from '@skeletonlabs/skeleton';
</script>

<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">
    ~
</svelte:fragment>
	<strong class="text-xl uppercase">rugby-algo</strong>
	<svelte:fragment slot="trail"><a
    id="button-t-b"
    class="btn btn-sm variant-ghost-surface"
    href="https://github.com/ThomasCombettes"
    target="_blank"
    rel="noreferrer"
>
    github
</a></svelte:fragment>
</AppBar>


