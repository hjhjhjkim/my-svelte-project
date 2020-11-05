<script>
  var count = 0;
  $: console.log(count);
  $: if (count >= 10) {
    alert("초과!");
    count = 0;
  }
  $: if (count < 0) {
    alert("!");
    count = 0;
  }
  var time = 0;
  function noodle() {
    time = setInterval(timer(), 1000);
  }
  function timer() {
    count = count - 1;
    document.getElementById("countdown").innerHTML = { count };
  }
</script>

<body>
  <p id="countdown">{count}</p>
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
