<script>
  export let fruits;
  export let reverse;
  export let slice;

  let computedFruits = [];
  let name = '';

  if (reverse) {
    computedFruits = [...fruits].reverse();
    name = 'reverse';
  } else if (slice) {
    computedFruits = fruits.slice(...slice.split(','));
    name = `slice ${slice}`;
  } else {
    computedFruits = fruits;
  }
</script>

<h2>
  Fruits {name}
</h2>

<ul>
  {#each computedFruits as fruit}
    <li>{fruit}</li>
  {/each}
</ul>

<style>
  h2 {
    color: orange;
  }
</style>
