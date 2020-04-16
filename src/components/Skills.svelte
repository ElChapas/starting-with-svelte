<script>
    let Skills = [
        {
            id: 1,
            name: 'HTML'
        },
        {
            id: 2,
            name: 'CSS'
        },
        {
            id: 3,
            name: 'JavaScript'
        }
    ]
</script>

<style>
    li {
            list-style: none;
        }
</style>

<div class="Skills">
    <h3>Habilidades: </h3>
    <ul>
        {#each Skills as {name}, i}
            <li>{name}</li>
        {/each}
    </ul>
</div>