<script>
	import { get_slot_changes } from 'svelte/internal';
import Card from './components/Card.svelte'
</script>

<main>
	<Card content='Card content 1'>
		<h2>Card content 1</h2>
	</Card>
	
	<Card content='Card content 2'>
		<h3>Card content 2</h3>
	</Card>

	<Card content='Card content 3'>
		<img src="https://picsum.photos/200" alt="Test">
	</Card>
	
	<Card content='Card content 4'>
		
	</Card>
	


</main>


<style>
	main{
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>