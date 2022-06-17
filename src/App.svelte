<script>
	import Keyboard from "./components/Keyboard.svelte";
	import Board from "./components/Board.svelte";

</script>


<main>
	<nav>notQuiteWordle</nav>
	<Board />
	<Keyboard />


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


