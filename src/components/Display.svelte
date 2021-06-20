<script>
  import { onDestroy } from 'svelte';
  import {count} from '../store/stores'

  let counter
  const unsubscribe = count.subscribe((value) => {
    counter = value
  })
  onDestroy(unsubscribe)
</script>

<h2>Current count is: {counter} </h2>
<!--// subscribe and unsubscribe can done with $ -->
<h2>Current count is: {$count} </h2>