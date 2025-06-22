<script lang="ts">
	import type { Snippet } from "svelte";

    type Props = {
        title: string;
        img_name: string;
        children?: Snippet;
    }

    let { title, img_name, children }: Props = $props();
</script>

<div class="advantage">
    <img
        class:smaller={!children}
        src={`/images/${img_name}.png`}
        alt="123"
    />
    <div class="text">
        <h3 class:bigger={!children}>{title}</h3>
        {#if children}
            <p>
                {@render children()}
            </p>
        {/if}
    </div>
</div>

<style>
    .advantage {
        padding: 5px;
        border-radius: 10px;
        /* background-color: #eee; */
        display: flex;
        gap: 15px;
        align-items: center;
    }

    img {
        min-width: 10%;
        width: 10%;
    }

    img.smaller {
        min-width: 7%;
        width: 7%;
    }

    .text {
        gap: 3px;
    }

    h3 {
        font-weight: 600;
    }

    h3.bigger {
        font-size: 20px;
        font-weight: 400;
    }
</style>