<script>
  export let initialCount, maxCount;

  let count = initialCount;
  $: msg = `You have clicked ${count} times`;
  
  function increment(){
    if(count === maxCount) return;
    count++;
  }
</script>

<button on:click={increment}>
  Clicks: {count}
</button>

<h3>{msg}</h3>