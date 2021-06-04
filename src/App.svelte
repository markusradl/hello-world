<script>
	import PostList from './components/PostList.svelte'
</script>

<main>
	<header>
		<p>Codevolution</p>
		<p>Svelte Tutorial - 27 - HTTP Request<p>
	</header>
	
	<section>
		<PostList />
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