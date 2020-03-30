<script>
	import { writable } from 'svelte/store'
	import Dog from './Dog.svelte'
	import Button from './Button.svelte'
	
	export let name;
	name = 'Svelte';

	const username = writable('Guest');
	username.set('Jun');
	
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
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
	<h1>Hello {name}!</h1>
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
</main>

<Dog />

<Button />
