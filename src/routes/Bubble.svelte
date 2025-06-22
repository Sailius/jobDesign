<script lang="ts">
    type Props = {
        order: 'first' | 'second'
    }

    let { order }: Props = $props();
</script>

<div class="bubble {order}"></div>

<style>
    .bubble {
        position: absolute;
        width: 1px;
        height: 1px;
    }

    .bubble.first {
        right: 0;
        top: 150px;
        animation: bubbles1 10s infinite;
        background-color: #76aeea55;
        box-shadow: 0 0 30px 20px #76aeea80;
    }

    .bubble.second {
        left: 0;
        top: 450px;
        background-color: #ffc06255;
        box-shadow: 0 0 30px 20px #ffc06280;
        animation: bubbles2 10s infinite;
    }

    @keyframes bubbles1 {
        0% {
            right: 0;
            top: 150px;
        }
        25% {
            right: 500px;
            top: 410px;
        }
        50% {
            right: 1500px;
            top: 250px;
        }
        75% {
            right: 800px;
            top: 50px;
        }
        100% {
            right: 0;
            top: 150px;
        }
    }

    @keyframes bubbles2 {
        0% {
            left: 0;
            top: 450px;
        }
        25% {
            left: 500px;
            top: 250px;
        }
        50% {
            left: 1500px;
            top: 410px;
        }
        75% {
            left: 1200px;
            top: 50px;
        }
        100% {
            left: 0;
            top: 450px;
        }
    }
</style>