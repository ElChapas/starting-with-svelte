<script>
    import Button from './Button.svelte' 
    let someText = `Road to Frontend developer `;
    let count = 0;
    let styles = { darkMode: false}

    function handleClick() {
        count += 1;
    }

    function toggle() {
        styles.darkMode = !styles.darkMode;
        window.document.body.classList.toggle("dark-mode")
    }

</script>

<style>
    p {
		color: #203D44;
		font-size: 2em
	}
</style>

<div class="About">
    <p>{someText}</p>

    <Button 
        on:click={handleClick} 
        count = {count} 
        text = "Add "
    />

    <Button 
        on:click={toggle} 
        text="DarkMode {styles.darkMode ? 'OFF' : 'ON'} " 
    />
</div>
