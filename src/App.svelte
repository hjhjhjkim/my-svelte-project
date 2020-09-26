<script>
  let number = 0;
  const add = () => {
    number++;
  };
  const minus = () => {
    number--;
  };
</script>

<style>
</style>

<p>{number}</p>
<button on:click={add}>+</button>
<button on:click={minus}>-</button>
