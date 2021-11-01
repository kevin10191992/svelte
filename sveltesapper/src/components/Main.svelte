<script>
  // your script goes here
  import Sidebar from "./Sidebar.svelte";
</script>

<main class="Main">
  <div class="Main-Container">
    <div class="Main-Content">
      <slot />
      <Sidebar />
    </div>
  </div>
</main>

<style>
  .Main-Container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }
  .Main-Content {
    margin: 2em 0 0 0;
    display: grid;
    grid-template-columns: 3fr 1fr;
    grid-gap: 60px;
    justify-content: space-between;
  }
</style>
