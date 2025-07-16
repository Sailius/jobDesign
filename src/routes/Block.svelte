<script lang="ts">
	import { onMount, type Snippet } from "svelte";

    type Props = {
        children?: Snippet;
    }

    let { children }: Props = $props();
</script>

<div>
    {#if children}
        {@render children()}
    {/if}
</div>

<style>
    div {
        position: relative;
        height: 100%;
        width: var(--procentage);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    
    div > :global(*) {
        z-index: 600;
    }
</style>
