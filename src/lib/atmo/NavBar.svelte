<script lang="ts">
    let { icon } = $props();
</script>

<div class="flex h-14 w-full border-b-[1px] border-border bg-sidebar">
    {@render icon()}
</div>
