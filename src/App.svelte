<script>
	import MovieItem from './Movie/item.svelte'
import { bind } from "svelte/internal";

	export let name;
	let texto = "soy la data reactiva"
</script>

<svelte:head>
	<title>Movies Svelte</title>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
</svelte:head>

<main class="conteiner">
	<div class="row">
		<MovieItem/>
	</div>
	
	<h1>Hello  {name}!</h1>
	<h5>{texto}</h5>
	<input type="text" bind:value={texto}>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>

</main>

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