<script lang="ts">
	import { type Snippet } from "svelte";

    type Props = {
        image_name: string;
        title: string;
        children: Snippet
    }

    let { image_name, title, children }: Props = $props();
</script>

<div class="plate">
    <img src={`/images/${image_name}.jpg`} alt="Внутрисалонная реклама на стикерах А4" />
    <div>
        <h3>{title}</h3>
        <p>
            {@render children()}
        </p>
    </div>
</div>

<style>
    .plate {
        /* margin-top: -20px; */
        cursor: pointer;
        height: 125px;
        width: 25%;
        display: flex;
        align-items: center;
        gap: 20px;
        justify-content: center;
        border-radius: 10px;
        transition: ease 0.25s;
    }

    .plate:hover {
        transform: scale(1.05);
    }

    .plate > div {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        gap: 5px;
    }

    h3 {
        font-weight: 600;
        font-size: 22px;
    }

    p {
        font-size: 18px;
    }

    img {
        height: 100px;
        border-radius: 5px;
    }

</style>