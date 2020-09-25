<script>
  let text = "";
  let number = 0;
  import First from "./first.svelte";
  import Second from "./second.svelte";
  import Third from "./third.svelte";
  import Fourth from "./fourth.svelte";
  import Fifth from "./fifth.svelte";
  import Sixth from "./six.svelte";
  import Seventh from "./seventh.svelte";
  import Eighth from "./eighth.svelte";
</script>

<style>
  .fontsize {
    font-size: (number);
  }

  #font1 {
    font-family: "Anton", sans-serif;
  }
  #font2 {
    font-family: "Nanum Myeongjo", serif;
  }
  #font3 {
    font-family: "Nanum Pen Script", cursive;
  }
  #font4 {
    font-family: "Open Sans Condensed", sans-serif;
  }
  #font5 {
    font-family: "Peddana", serif;
  }
  #font6 {
    font-family: "Ranchers", cursive;
  }
  #font7 {
    font-family: "Roboto Condensed", sans-serif;
  }
  #font8 {
    font-family: "Source Code Pro", monospace;
  }
</style>

<div class="container">
  <section>
    <label for="letter">text</label>
    <input id="letter" type="text" bind:value={text} />
    <label for="font">fontsize</label>
    <input id="font" type="number" bind:value={number} />
    <h1>{number === undefined ? 0 : number}px</h1>

    <br />
    <input type="text" placeholder={text} id="font1" />
    <input type="text" placeholder={text} id="font2" />
    <input type="text" placeholder={text} id="font3" />
    <input type="text" placeholder={text} id="font4" />
    <input type="text" placeholder={text} id="font5" />
    <input type="text" placeholder={text} id="font6" />
    <input type="text" placeholder={text} id="font7" />
    <input type="text" placeholder={text} id="font8" />
  </section>
</div>
