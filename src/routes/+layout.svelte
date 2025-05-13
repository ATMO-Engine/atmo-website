<script lang="ts">
    import NavBar from "$lib/atmo/NavBar.svelte";
    import RowIcon from "$lib/atmo/icons/RowIcon.svelte";
    import "../app.css";
    import { ModeWatcher } from "mode-watcher";
    let { children } = $props();
</script>

<ModeWatcher />

<NavBar>
    {#snippet icon()}
        <RowIcon />
    {/snippet}
</NavBar>

{@render children()}
