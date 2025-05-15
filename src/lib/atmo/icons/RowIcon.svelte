<script lang="ts">
    import { mode } from "mode-watcher";
</script>

{#if mode.current === "dark"}
    <img
        fetchpriority="high"
        width="48"
        src="/icons/atmo-dark.svg"
        alt="atmo row icon for dark mode"
    />
{:else if mode.current === "light"}
    <img
        fetchpriority="high"
        width="48"
        src="/icons/atmo-light.svg"
        alt="atmo row icon for light mode"
    />
{/if}
