<script>
	import Card from './components/Card.svelte'
</script>

<main>
	<Card><h2>Card content 1</h2></Card>
	<Card><h3>Card content 2</h3></Card>
	<Card><img src="https://picsum.photos/200" alt="Test"></Card>
	<Card />

	<Card>
		<div slot="header">
			<h3>Header</h3>
		</div>
		<div slot="content">
			<img src="https://picsum.photos/200" alt="Test">
		</div>
		<div slot="footer">
			<button>View details</button>
		</div>
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