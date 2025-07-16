<script lang="ts">
	import { onMount, type Snippet } from "svelte";

    type Props = {
        type: number;
        children?: Snippet;
    }

    let { type, children }: Props = $props();
</script>

<div class={`type${type}`}>
    {#if children}
        {@render children()}
    {/if}
</div>

<style>
    div {
        width: 100%;
        height: var(--procentage);
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