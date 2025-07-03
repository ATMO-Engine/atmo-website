<script lang="ts">
    let { icon } = $props();

    import Sun from "@lucide/svelte/icons/sun";
    import Moon from "@lucide/svelte/icons/moon";

    import { toggleMode } from "mode-watcher";
    import { Button } from "$lib/components/ui/button";
</script>

<header class="sticky top-0 z-10 border-b border-border bg-sidebar">
    <div class="container flex h-14 w-full flex-row">
        <a class="flex shrink flex-row items-center gap-4 p-2" href="/">
            {@render icon()}
            <span class="font-[AmaticSC] text-4xl font-bold"> ATMO Engine </span>
            <!-- <Button>Download</Button> -->
        </a>
        <div class="ml-auto flex h-full w-auto items-center justify-end gap-4 pr-2">
            <Button onclick={toggleMode} variant="outline" size="icon">
                <Sun
                    class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
                />
                <Moon
                    class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
                />
            </Button>
        </div>
    </div>
</header>
