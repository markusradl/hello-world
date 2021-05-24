<script>
  import { getContext} from 'svelte'

  const userName = getContext('userName')
</script>

<main>
  <h2>Child F Component</h2>
  <h2>Child F Username from App: {userName}</h2>
</main>