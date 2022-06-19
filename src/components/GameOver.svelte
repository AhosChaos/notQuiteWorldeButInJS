<script>
    import { gameInfo, GAME_WORD, guess, createGrid, board, gameOver, colors, WORD_LIST} from "../store"
    import Board from "./Board.svelte"
    const playAgain = () => {
        gameInfo.set({
            attempt: 0, char: 0
        });
        const word = WORD_LIST[Math.floor(Math.random() * WORD_LIST.length)]
        GAME_WORD.set(word)

        guess.set("");
        colors.set(createGrid());
        board.set(createGrid());
        gameOver.set(false);
    }

</script>

<div>
    <Board />

</div>

<div class="center">
    <h3>The correct word was: <strong>{$GAME_WORD}</strong></h3>
    <h3>You guess: <strong>{$guess}</strong></h3>
    <div class="center">
        <button on:click={playAgain}>Play Again?</button>
    </div>
    
</div>

<style>
    strong {
        font-weight: 900;
    }
    h3 {
        font-size:  2em;
    }

    button{
        background-color: var(--orange);
        color: white;
        margin-top: 20px;
        padding: 20px 50px;
        cursor: pointer;
        border: none;
    }

    .center {
        margin: 20px auto;
        width: fit-content;
        text-align: center;
    }


</style>