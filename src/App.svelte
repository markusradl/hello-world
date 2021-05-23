<script>
	let count = 0

	function handleClick(event, stepSize) {
		count += stepSize
		console.log(event)
	}
</script>

<main>
	<!-- In Line Event handler -->
	<button on:click={() => (count = count + 1)} >Count up! Value: {count}</button>
  
	<button on:click={(event) => handleClick(event, 5)} >Count up by 5! Value: {count}</button>
	<button on:click={(event) => handleClick(event, 10)} >Count up by 10! Value: {count}</button>

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