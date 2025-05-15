<script lang="ts">
    import NavBar from "$lib/atmo/NavBar.svelte";
    import RowIcon from "$lib/atmo/icons/RowIcon.svelte";
    import { ModeWatcher } from "mode-watcher";
    import "../app.css";

    let { children } = $props();
</script>

<ModeWatcher />

<NavBar>
    {#snippet icon()}
        <RowIcon />
    {/snippet}
</NavBar>

<div class="container mt-4 h-full">
    {@render children()}
</div>
