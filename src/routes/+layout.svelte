<script lang="ts">
    import NavBar from "$lib/atmo/NavBar.svelte";
    import "../app.css";
    import { ModeWatcher } from "mode-watcher";
    let { children } = $props();
</script>

<ModeWatcher />

<NavBar>
    {#snippet icon()}
        ATMO Engine
    {/snippet}
</NavBar>

{@render children()}
