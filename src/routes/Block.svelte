<script lang="ts">
	import { onMount, type Snippet } from "svelte";

    type Props = {
        procentage: number;
        children?: Snippet
    }

    let { procentage, children }: Props = $props();
    
    let block: HTMLDivElement;
    onMount(() => {
        block.style.width = `${procentage}%`;
        block.style.visibility = 'visible';
    });
</script>

<div bind:this={block}>
    {#if children}
        {@render children()}
    {/if}
</div>

<style>
    div {
        position: relative;
        visibility: hidden;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    
    div > :global(*) {
        z-index: 600;
    }
</style>
