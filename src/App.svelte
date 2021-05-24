<script>
	import Greet from './components/Greet.svelte'	
	const name = 'Markus'
	const organisation = 'mrsln'
	const obj = {
		name: 'Barry',
		heroName: 'Flash'
	}
</script>

<main>
	<Greet name='Bruce' heroName='Batman'/>
	<Greet name='CLark'heroName='Superman'/>
	<Greet name='Diana' heroName='Wonder Woman'/>
	<Greet {name}/>
	<!--Spread operator ... extracts the items out of the ohject-->
	<Greet {...obj}/>


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