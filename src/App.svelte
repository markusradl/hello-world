<script>
	import Tab1 from './components/Tab1.svelte'
	import Tab2 from './components/Tab2.svelte'
	import Tab3 from './components/Tab3.svelte'

	let selectedTab = Tab1
</script>

<main>
	<header>
		<p>Codevolution</p>
		<p>Svelte Tutorial - 29 - dynamic components<p>
	</header>
		
	<section>
		<button on:click={() => selectedTab = Tab1}>Tab1</button>
		<button on:click={() => selectedTab = Tab2}>Tab2</button>
		<button on:click={() => selectedTab = Tab3}>Tab3</button>

		<svelte:component this={selectedTab} />
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