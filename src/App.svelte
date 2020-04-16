<script>
	import About from "./components/About.svelte";
	import Text from "./components/Text.svelte";
	import Person from "./components/Person.svelte";
	import Skills from "./components/Skills.svelte";
	import Input from "./components/Input.svelte";
	import Photos from "./components/Photos.svelte";
	import ButtonCount from "./components/ButtonCount.svelte";
	
	export let name;
	export let lastName;

	const data = {
		name: 'Oscar',
		LastName: 'Chapa',
		age: 19
	}

</script>

<style>
	:global(body) {
		background-color: beige;
		color: #203D44;
	}

	:global(:root) {
		--theme-color: rgb(241, 101, 101);
	}

	:global(body.dark-mode) {
		background-color: #203D44;
		color: white
	}

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: var(--theme-color);
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Hello! I'm {name} {lastName}!</h1>
	<About />
	<Text anotherText="Hello!"/>
	<Person {...data} />
	<Skills />
	<Input />
	<ButtonCount />
	<h2>Photos</h2>
	<Photos />
</main>