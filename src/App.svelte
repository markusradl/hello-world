<script>
	import Counter, { getTotalCount } from './components/Counter.svelte'
</script>

<main>
	<header>
		<p>Codevolution</p>
		<p>Svelte Tutorial - 30 - module context<p>
	</header>
		
	<section>
		<button on:click={() => {alert(getTotalCount())}}>Show total count</button>
		<hr>
		<Counter />
		<Counter />
		<Counter />
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