<script>
  let count = 0;

  const add = () => {
    count++;
  };
  const minus = () => {
    count--;
  };
</script>

<style>
</style>

<div class="container">
  <section>
    <h1>#1. Event Listener</h1>

    <div class="wrapper">
      <article class="click">
        <p>{count}</p>
        <button on:click={add}>+</button>
        <button on:click={minus}>-</button>
      </article>
    </div>
  </section>
</div>
