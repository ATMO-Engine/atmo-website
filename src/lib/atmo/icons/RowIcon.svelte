<script lang="ts">
    import { mode } from "mode-watcher";
</script>

{#if mode.current === "dark"}
    <img class="h-full max-w-32" src="/icons/atmo-row-dark.png" alt="atmo row icon for dark mode" />
{:else if mode.current === "light"}
    <img
        class="h-full max-w-32"
        src="/icons/atmo-row-light.png"
        alt="atmo row icon for light mode"
    />
{/if}
