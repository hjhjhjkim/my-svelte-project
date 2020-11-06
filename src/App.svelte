<script>
  var count = 0;
  $: console.log(count);
  $: if (count >= 60) {
    alert("초과!");
    count = 0;
  }
  $: if (count < 0) {
    alert("!");
    count = 0;
  }

  var time = 0;
  var counts = 0;
  function onclick() {
    counts = parseInt(document.getElementById("countdown").value);
    time = setInterval(timer(), 1000);
  }
  function timer() {
    document.getElementById("countdown").innerHTML = counts;
    counts = counts - 1;

    if (counts == 0) {
      clearInterval(time);
      alert("Time Over");
    }
  }
</script>

<style>
  .circle {
    width: 100px;
    height: 100px;
    border: 3pt;
    border-radius: 50px;
  }
</style>

<body class="circle">
  <input id="countdown" value={count} />
  <button
    on:click={() => {
      count++;
    }}>+</button>

  <button
    on:click={() => {
      count--;
    }}>-</button>
  <button onclick="onclick()">start!</button>
</body>
