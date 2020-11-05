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
  function noodle() {
    clearInterval(time);
    time = setInterval(timer(), 1000);
  }
  function timer() {
    count = count - 1;
    document.getElementById("countdown").innerHTML = count;
    if (count == 0) {
      clearInterval(time);
      alert("Time Over");
    }
  }
</script>

<body>
  <input id="countdown" value={count} />
  <button
    on:click={() => {
      count++;
    }}>+</button>

  <button
    on:click={() => {
      count--;
    }}>-</button>
  <input type="button" value="start!" onclick="noodle()" />
</body>
