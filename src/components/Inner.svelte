<script>
  import {createEventDispatcher} from 'svelte'

  const dispach = createEventDispatcher()
  function greet() {
    dispach('greet', 'Hello')
  }
</script>

<button on:click={greet}>Greet</button>