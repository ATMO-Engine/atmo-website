<script lang="ts">
    import { m } from "$lib/paraglide/messages.js";
    import { Button } from "$lib/components/ui/button";
    import { ArrowRight } from "@lucide/svelte";
    import { AspectRatio } from "$lib/components/ui/aspect-ratio";
    import { appState } from "@/stores/app.svelte";
</script>

<div class="flex h-full w-full flex-col items-center justify-center">
    {#if appState.width >= 1024}
        <AspectRatio
            ratio={16 / 9}
            class="flex w-full flex-col items-center justify-center gap-4 rounded-lg border-2 border-border bg-gradient-to-tl from-accent to-accent/50"
        >
            <span class="text-6xl">{m.creation()}</span>
            <!-- <Button href="/download">
                <span>
                    {m.download()}
                </span>
                <ArrowRight />
            </Button> -->
            <Button href="https://discord.gg/fvQj9F2jMJ" target="_blank">
                <span>
                    {m.join_our_discord()}
                </span>
                <ArrowRight />
            </Button>
        </AspectRatio>
    {:else}
        <div class="flex h-full w-full flex-col items-center justify-center gap-2">
            <span class="text-2xl">{m.creation()}</span>
            <Button href="https://discord.gg/fvQj9F2jMJ" target="_blank">
                <span>
                    {m.join_our_discord()}
                </span>
                <ArrowRight />
            </Button>
        </div>
    {/if}
</div>
