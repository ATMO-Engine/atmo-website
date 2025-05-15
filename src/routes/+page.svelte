<script lang="ts">
    import { m } from "$lib/paraglide/messages.js";
    import { Button } from "$lib/components/ui/button";
    import { ArrowRight } from "@lucide/svelte";
    import { AspectRatio } from "$lib/components/ui/aspect-ratio";
</script>

<div class="flex h-full w-full flex-col items-center justify-center">
    <AspectRatio
        ratio={16 / 9}
        class="flex w-full flex-col items-center justify-center gap-4 rounded-lg border-2 border-border bg-gradient-to-tl from-accent to-accent/50"
    >
        <span class="text-6xl">{m.creation()}</span>
        <Button href="/download">
            <span>
                {m.download()}
            </span>
            <ArrowRight />
        </Button>
    </AspectRatio>
</div>
