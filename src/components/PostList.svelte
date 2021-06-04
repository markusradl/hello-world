<script>
  import { onMount } from 'svelte'
import { identity } from 'svelte/internal';
  
  let posts = []


  onMount(async() => {

    // await because the fetch API returns a promise
    const response = await fetch('http://jsonplaceholder.typicode.com/posts')
    posts = await response.json()
    console.log(posts)
  })

</script>


{#each posts as post (post.id)}
  <h3>{post.id}. {post.title}</h3>
  <p>{post.body}</p>
  <hr />
  {:else}
    <p>loading...</p>
{/each}

