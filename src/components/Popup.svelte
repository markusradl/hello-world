<script>
  import { createEventDispatcher } from 'svelte'

  const dispatch = createEventDispatcher()
</script>

<div>
  <h2>This is a POPUP</h2>
  <button on:click={() => (dispatch('close', 'Data send to parent is this'))}>Close Popup</button>
</div>


