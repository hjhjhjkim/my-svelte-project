<script>
  let count = 0;
  $: console.log(count);
  $: if (count >= 60) {
    alert("초과!");
    count = 0;
  }
  $: if (count < 0) {
    alert("!");
  }
</script>

<style>
</style>

<div class="container">
  <section>
    <h1>#3 Reactivity Statements</h1>
    <p>{count}</p>
    <button
      on:click={() => {
        count++;
      }}>
      +
    </button>
    <button
      on:click={() => {
        count--;
      }}>-</button>
  </section>
</div>
