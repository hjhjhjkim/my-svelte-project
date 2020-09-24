<script>
  let text = "";
  let number = 0;
</script>

<style>
  .fontsize {
    font-size: (number);
  }
</style>

<div class="container">
  <section>
    <h1>#6 InputBinding</h1>

    <label for="letter">text</label>
    <input id="letter" type="text" bind:value={text} />
    <label for="font">fontsize</label>
    <input id="font" type="number" bind:value={number} />

    <br />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
    <input type="text" placeholder={text} class="fontsize" />
  </section>
</div>
