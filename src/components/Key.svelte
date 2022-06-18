<script>
    export let char;
    export let keyPress;
</script>

<div class="key" on:click={() => keyPress(char.toUpperCase())}>
    {char.toUpperCase()}
</div>

<style>
    .key {
        background-color: var(--bg);
        color: white;
        padding: 20px 18px;
        margin: 4px;
        cursor: pointer;
        border-radius: 4px;
        transition: background-color .3s;
    }

    .key:hover{
        background-color: var(--orange);
    }

</style>
