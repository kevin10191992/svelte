<script>
  // your script goes here
</script>

<footer class="Footer">
  <div class="Footer-Container">
    <div class="Footer-Content">
      <div class="Footer-Copy">Hecho con amor.</div>
      <div class="Footer-Svelte">
        Echo con Svelte.js
        <img src="svelte.png" alt="svelte" />
      </div>
    </div>
  </div>
</footer>

<!-- markup (zero or more items) goes here -->
<style>
  /* your styles go here */

  .Footer {
    background-color: rgba(28, 41, 56, 0.8);
    color: white;
    padding: 1.5em 0;
    margin: 2em 0 0 0;
    font-size: 13px;
    font-weight: 300;
  }
  .Footer-Container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }

  .Footer-Content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .Footer-Svelte {
    display: flex;
    align-items: center;
  }

  .Footer-Svelte img {
    margin: 0 0 0 0.5em;
  }
</style>
