<script>
    export let name = "World"
</script>

<div class="Input">
    <input type="text" bind:value={name}>
    <h3>Hello {name}!</h3>
</div>