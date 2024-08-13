<script>
  import Counter from './lib/Counter.svelte'
  const name = 'Svelte'
</script>

<h1>Hello {name}!</h1>
<Counter initialCount={3} maxCount={10}/>

<style>

</style>