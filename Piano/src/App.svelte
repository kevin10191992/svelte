<script>
  let teclas = [
    { Numero: 1, Color: "red" },
    { Numero: 2, Color: "orange" },
    { Numero: 3, Color: "yellow" },
    { Numero: 4, Color: "green" },
    { Numero: 5, Color: "teal" },
    { Numero: 6, Color: "blue" },
    { Numero: 7, Color: "purple" },
  ];

  function Sonar(Numero) {
    const audio = new Audio();
    audio.src = `assets/sonidos/note${Numero}.wav`;
    audio.load();
    audio.play();
  }
</script>

<main>
  <div class="container mt-5">
    <div class="row">
      <div class="col-lg-6 mx-auto">
        <ul class="list-group">
          {#each teclas as t}
            <li
              class="list-group-item list-group-item-action"
              style="background-color: {t.Color};"
              on:click={() => Sonar(t.Numero)}
            />
          {/each}
        </ul>
      </div>
    </div>
  </div>
</main>

<style>
  .list-group-item {
    cursor: pointer;
    height: 50px;
  }
</style>
