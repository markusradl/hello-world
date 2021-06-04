<script>
	import Autofocus from './components/Autofocus.svelte';
import AutoFocus from './components/Autofocus.svelte'
</script>

<main>
	<header>
		<p>Codevolution</p>
		<p>Svelte Tutorial - 28 - this binding<p>
	</header>
	
	<section>
		<Autofocus />
	</section>
</main>


<style>

	h4 {
		color: orange;
	}
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