<script>
    import { onMount } from 'svelte';

    let photos = []

    onMount( async () => {
        const response = await fetch('https://jsonplaceholder.typicode.com/photos?_limit=20')
        photos = await response.json()
        console.log(photos);
    })

</script>

<style>
    .Photos {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        justify-items: center
    }

    img {
        width: 100px;
        height: 100px;
    }
</style>


<div class="Photos">
    {#each photos as photo}
        <figure>
            <img src={photo.url} alt={photo.title}>
            <figcaption>{photo.title}</figcaption>
        </figure>
    {:else}
        <p>loading...</p>
    {/each}
</div>