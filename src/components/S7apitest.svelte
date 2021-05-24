<script>
import { onMount } from "svelte";

  let answer = ''
  let messageId = 0

  async function login(){
    alert('Start login')
      await fetch(
      'https://10.0.0.190/api/jsonrpc',
      {
        method : 'POST',
        headers: {
          'Content-type': 'application/json',
        },
        body: JSON.stringify({
          "id": messageId++,
          "jsonrpc": "2.0",
          "method": "Api.Login",
          "params": {
            user: 'Everybody',
            password: '',
            'include_web_application_cookie': true
          }
        })
      })
      .then(r => {
        if (!r.ok){
          throw new Error('Network response was not ok')
        }
        return r.json()
      })
      .then((data) => {
        console.log(data)
        answer = data
      })
      .catch((error) => {
        console.log('Error:', error)
      })
   }

</script>

<main>

  <button on:click={login}>Login</button>
  <h2>{answer}</h2>

</main>