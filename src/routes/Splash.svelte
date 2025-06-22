<script lang="ts">
	import { onMount, type Snippet } from "svelte";

    type Props = {
        procentage: number;
        type: number;
        children?: Snippet
    }

    let { procentage, type, children }: Props = $props();
    
    let block: HTMLDivElement;
    onMount(() => {
        block.style.height = `${procentage}%`;
        block.style.visibility = 'visible';
    });
</script>

<div bind:this={block} class={`type${type}`}>
    {#if children}
        {@render children()}
    {/if}
</div>

<style>
    div {
        width: 100%;
        visibility: hidden;
        border: 2px solid #ffe;
        padding: 15px;
        border-radius: 10px;
    }

    div.type1 {
        background: linear-gradient(180deg, #d9f9db, #eee 50%);
    }

    div.type2 {
        background: linear-gradient(135deg, #d9f9db -50%, #eee 50%);
    }
</style>