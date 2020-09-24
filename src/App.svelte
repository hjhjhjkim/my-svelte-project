<script>
  import first from "./first.svelte";
  import second from "./second.svelte";
</script>

<style>
  h1:first-child {
    font-family: "Do Hyeon", sans-serif;
  }
  h1:last-child {
    font-family: "Nanum Pen Script", cursive;
  }
</style>

<h1>1번 폰트입니다.</h1>
<h1>2번 폰트입니다.</h1>
<h2>{first}</h2>
<h2>{second}</h2>
