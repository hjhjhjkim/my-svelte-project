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
  <button onclick="noodle()">start!</button>
  <script>
    var time = 0;
    function noodle() {
      clearInterval(time);
      time = setInterval(timer(), 1000);
    }
    function timer() {
      document.getElementById("countdown").innerHTML = count = count - 1;

      if (count == 0) {
        clearInterval(time);
        alert("Time Over");
      }
    }
  </script>
</body>
