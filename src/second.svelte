<script>
  let count = 0;
  $: double = count * 2;
</script>

<style>
</style>

<div class="container">
  <section>
    <h1>#2 Reactivity Declaration</h1>
    <p>횟수: {count}</p>
    <p>횟수*2: {double}</p>
    <button
      on:click={() => {
        count++;
      }}>
      +
    </button>
  </section>
</div>
