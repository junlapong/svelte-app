<script>
let count = 0

const incrementCount = () => {
  count++;
}

$: {
  console.log(`the count is ${count}`)
  console.log(`double the count is ${count * 2}`)
}
</script>

<style>
#container {
  text-align: center;
}

#count {
  font-size: 200%;
}

button {
    cursor: pointer;
}

</style>

<div id="container">
    <button on:click={incrementCount}>A button</button>
    <div id="count">{count}</div>
</div>