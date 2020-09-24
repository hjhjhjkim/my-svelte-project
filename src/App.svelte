<script>
  let text = "";
  let number = 0;
  import First from "./first.svelte";
</script>

<style>
  .fontsize {
    font-size: (number);
  }

  h1 {
    font-family: "Anton", sans-serif;
  }
  /*font-family: "Nanum Myeongjo", serif;
  font-family: "Nanum Pen Script", cursive;
  font-family: "Open Sans Condensed", sans-serif;
  font-family: "Peddana", serif;
  font-family: "Ranchers", cursive;
  font-family: "Roboto Condensed", sans-serif;
  font-family: "Source Code Pro", monospace;*/
</style>

<div class="container">
  <section>
    <h1>#6 InputBinding {First}</h1>

    <label for="letter">text</label>
    <input id="letter" type="text" bind:value={text} />
    <label for="font">fontsize</label>
    <input id="font" type="number" bind:value={number} />
    <h1>{number === undefined ? 0 : number}px</h1>

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
