<script>
	let firstName = 'Markus'
	let lastName = 'Radl'

	let items = [
		{
			id: 1,
			tile: 'TV',
			price: 100
		},
		{
			id: 2,
			tile: 'Phone',
			price: 200
		},
		{
			id: 3,
			tile: 'Laptop',
			price: 300
		}
	]

	$: fullName = `${lastName} ${firstName}`
	$: {
		const greet = `Fullname is ${firstName} ${lastName}`
		console.log(greet)
	}
	$: total = items.reduce((total, curr) => (total = total + curr.price),0)

	let volume = 0
	$:if (volume < 0) {
			alert('You can not go under 0')
			volume = 0
		}else if (volume > 20) {
			alert('You can not go higher than 20')
			volume = 20
		}
</script>

<main>

	<h2>Current volume: {volume}</h2>
	<div>
		<button on:click={() => volume += 2}>Increase volume (+)</button>
		<button on:click={() => (volume -= 2)}>Decrease volume (-)</button>
	</div>

	<button 
		on:click={() => {
			firstName = 'Clark'
			lastName = 'Kent'
		}}>Change name</button
	>
	
	<h2>{firstName} {lastName}</h2>
	<h2>{fullName}</h2>

	<button on:click={() => items = ([...items,{id:4, title: 'Keyboard', price: 50}])}>Add item</button>

	<h2>Calc total Price with reduce</h2>
	<h2>Total: {total}</h2>

</main>

<style>
	main {
		/*text-align: center;*/
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