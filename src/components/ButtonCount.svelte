<script>
    import { count } from '../store/store.js'

    function handleClick() {
        count.update(n => n + 1);
    }

</script>

<style>
    button {
        border: none;
        background-color: coral;
        color: white;
        border-radius: 5%;
        font-size: 2em;
        cursor: pointer;
    }
</style>

<button on:click={handleClick}>
    Click {$count === 0 ? '' : $count}
</button>