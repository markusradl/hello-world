<script>
	const name = 'Maxx'
	const channel = '<b>mrsln<b>'
	const hack =`<a href="#" onclick="alert('You have been hacked')">Win a prize<a>`
	const headingID = 'heading'
	const id = 'heading1'
	const disabled = true
	const status = 'success'
	const isPromoted = false
	const promoted = true
</script>

<main>
	<h2 class="underline">Underlined Text</h2>
	<h2 class="{status}">Status</h2>
	<h2 class="{isPromoted ? 'promoted' : ''}">Movie Title - Contionial class</h2>
	<h2 class:promoted={isPromoted}>Conditional binding short hand</h2>
	<h2 class:promoted>Shorter hand, if variable and class has the same name</h2>
	<h1>Hello {2 * 3 + name}</h1>
	<div>{@html channel}</div>
	<div>{@html hack}</div>
	<h2 id={headingID}>This is a Heading with id-tag heading</h2>
	<h2 {id}>This is the same tag as above with dynamic id - short hand notation</h2>
	<button disabled={disabled}>Binding short hand notation</button>
		
</main>

<style>
	.underline {
		text-decoration: underline;
	}

	.danger {
		color: #ff3e00;
	}

	.success {
		color: darkgreen;
	}	

	.promoted {
		font-style: italic;
	}

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