<script>
    import { board, colors, gameOver } from "../store"
    export let x;
    export let y;
    $: letter = $board[y][x]
    $: color = $colors[y][x]

</script>


<div class={`cell ${color}`}>
    {#if !$gameOver}
        {letter}
    {/if}

</div>


<style>
    .cell{
        width: 70px; height: 70px;
        color: white;
        background-color: var(--bg);
        margin: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 55px;
        border-radius: 5px;
        transition: background-color .7s;
    }

    .correct {
        background-color: var(--green);
    }
    .close {
        background-color: var(--orange);
    }
    .incorrect {
        background-color: var(--dark);
    }


</style>


