<script context="module">
  let totalCount = 0

  export function getTotalCount() {
    return totalCount
  }
</script>
<script>
  let count = 0

  function handleClick() {
    count += 1
    totalCount += 1
  }
</script>

<button on:click={handleClick}>Increment</button>
<h3>Counter value: {count}</h3>