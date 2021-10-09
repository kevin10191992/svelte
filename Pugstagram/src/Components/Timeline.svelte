<script>
  // your script goes here
  import Card from "./Card.svelte";
  export let Post = [];
</script>

<div class="Timeline">
  <div class="Timeline-Container">
    {#each Post as p}
      <Card {...p} />
    {:else}
      <div>...Cargando</div>
    {/each}
  </div>
</div>

<style>
  .Timeline {
    padding: 4em 0 0 0;
  }
</style>
