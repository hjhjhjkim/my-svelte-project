<script>
  let text = "";
  let number = 0;
  import First from "./first.svelte";
  import Second from "./second.svelte";
  import Third from "./third.svelte";
</script>

<style>
  .fontsize {
    font-size: (number);
  }

  h1 {
    font-family: "Anton", sans-serif;
  }
  h2 {
    font-family: "Nanum Myeongjo", serif;
  }
  h3 {
    font-family: "Nanum Pen Script", cursive;
  }
  input::placeholder {
    font-family: "Anton", sans-serif;
  }
  /*
  font-family: "Open Sans Condensed", sans-serif;
  font-family: "Peddana", serif;
  font-family: "Ranchers", cursive;
  font-family: "Roboto Condensed", sans-serif;
  font-family: "Source Code Pro", monospace;*/
</style>

<div class="container">
  <section>
    <h1>#6 InputBinding</h1>
    <h2>inputbinding font2</h2>
    <h3>input font3</h3>

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
