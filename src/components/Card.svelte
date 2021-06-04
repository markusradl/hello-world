<script>
  export let content
</script>

<div class="card">{content} <p>With props only String </p> </div>

<div class="card">
  <slot>
    Default slot content, no slot data defined in parent
  </slot> 
  <p>With slots everything</p>
</div>

<style>
  .card {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    transition: 0.3s;
    padding: 16px;
    margin-bottom: 20px;
    width: 200px;
  }

  .card:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }
</style>