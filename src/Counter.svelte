<script>
  let count = 0;
  const handler = () => count++;

  $: doubled = count * 2;
</script>

<p>
  Count clicked:
  <strong>{count}</strong>
   {count > 1 ? 'times' : 'time'}
</p>

<button on:click={handler}>Click</button>
<p>Double of count is {doubled} </p>
