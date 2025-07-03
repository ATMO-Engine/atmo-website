<script lang="ts">
    import NavBar from "$lib/atmo/NavBar.svelte";
    import RowIcon from "$lib/atmo/icons/RowIcon.svelte";
    import { ModeWatcher } from "mode-watcher";
    import "../app.css";
    import { appState } from "@/stores/app.svelte";

    let { children } = $props();

    let width = $state(0);

    $effect(() => {
        appState.width = width;
    });
</script>

<ModeWatcher />
<svelte:window bind:innerWidth={width} />

<NavBar>
    {#snippet icon()}
        <RowIcon />
    {/snippet}
</NavBar>
<div class="container mt-4 h-full">
    {@render children()}
</div>
