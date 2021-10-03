<script>
  let diceIz = "dice1";
  let diceDer = "dice2";

  function Tirar() {
    diceIz = `dice${getRandomArbitrary(1, 6)}`;
    diceDer = `dice${getRandomArbitrary(1, 6)}`;
  }

  function getRandomArbitrary(min, max) {
    return Math.round(Math.random() * (max - min) + min);
  }
</script>

<main>
  <div class="container">
    <div class="row">
      <div class="col-12 text-center m-3">
        <button class="btn btn-success lg m-3" on:click={Tirar}
          >Tirar Dados</button
        >
      </div>

      <div class="col-12 text-center">
        <img src={`./assets/img/${diceIz}.png`} alt="Dado_1" />
        <img src={`./assets/img/${diceDer}.png`} alt="Dado_2" />
      </div>
      {#if diceIz == diceDer}
        <div class="col-12 text-center">
          <div class="alert alert-success" role="alert">
            <h1>Ganaste</h1>
          </div>
        </div>
      {/if}
    </div>
  </div>
</main>

<style>
  img {
    width: 300px;
    height: 300px;
    background-color: red;
    margin: 30px;
    border-radius: 20px;
  }
</style>
