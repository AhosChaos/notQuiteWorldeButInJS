<script>
	import { gameOver, GAME_WORD, WORD_LIST } from "./store";
	import { fade } from "svelte/transition";
	import Keyboard from "./components/Keyboard.svelte";
	import Board from "./components/Board.svelte";
	import GameOver from "./components/GameOver.svelte";
	const word = WORD_LIST[Math.floor(Math.random() * WORD_LIST.length)];
    GAME_WORD.set(word);


</script>


<main>
	<nav>notQuiteWordle</nav>
	
	

	{#if $gameOver}
		<GameOver />
	{:else}
		<div in:fade={{duration: 800}}>
			<Board />
			<Keyboard />
		</div>
	{/if}


</main>

<style>
	nav{
		background-color: var(--bg);
		color: white;
		font-weight: bold;
		padding: 15px;
		font-size: 2em;
		text-align: center;
	}


</style>


