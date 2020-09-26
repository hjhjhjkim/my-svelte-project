<script>
  let text = "";
  let number = 0;
  /*  import First from "./first.svelte";
  import Second from "./second.svelte";
  import Third from "./third.svelte";
  import Fourth from "./fourth.svelte";
  import Fifth from "./fifth.svelte";
  import Sixth from "./six.svelte";
  import Seventh from "./seventh.svelte";
  import Eighth from "./eighth.svelte";*/
</script>

<style>
  /* input::placeholder {
    font-size: {number === undefined ? 0 : number}px" ;
  }*/
  /* svelte style에서 자바스크립트 변수를 활용하기 위한 노력들이 눈에 보입니다.. */
  /* 결론부터 말씀드리자면, 별도 라이브러리 없이 인라인 스타일을 활용하지 않고서는 불가능합니다.. */
  .block {
    display: inline-block;
    width: 200px;
    height: 100px;
    font-size: var(--font-size);
  }
  
  label {
    display: inline;
  }
  /*section {
    display: flexbox;
    justify-content: space-between;
  }*/

  form {
    margin: 40px;
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
    position: relative;
    top: -4px;
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
  <form>
    <label for="letter">text</label>
    <input id="letter" type="text" bind:value={text} />
    <label for="font">font size(px)</label>
    <input id="font" type="number" bind:value={number} />
  </form>

  <br />
  <section>
    <!-- 사용하신 방법을 적용하기 위해서는 아래와 같이 가능합니다 -->
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font1" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font2" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font3" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font4" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font5" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font6" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font7" class="block" />
    <input type="text" placeholder={text} style="--font-size: {number}px" id="font8" class="block" />
  </section>
</div>
