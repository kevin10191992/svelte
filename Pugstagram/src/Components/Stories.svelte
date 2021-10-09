<script>
  // your script goes here
</script>

<div class="Stories">
  <div class="Stories-Container">
    <div class="Stories-Head">
      <h2>Historias</h2>
      <span> Ver todas </span>
    </div>
    <div class="Stories-Items">
      <div class="Stories-Item">
        <div class="Stories-Item-Box">
          <img
            src="https://www.estrellaroja.com.mx/general/img/avatar/avatar-h.png"
            alt="Stories"
          />
        </div>
        <h2>
          kperez
          <span>10 horas antes</span>
        </h2>
      </div>
    </div>
  </div>
</div>

<!-- Stories.svelte -->
<style>
  .Stories {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    margin: 1em 0;
    padding: 0.5em 1em;
    background-color: white;
  }
  .Stories-Item img {
    width: 32px;
    height: 32px;
    border-radius: 50%;
  }
  .Stories-Item {
    display: flex;
    align-items: center;
    margin: 0 0 0.5em 0;
  }
  .Stories-Item h2 {
    font-size: 14px;
    color: black;
    margin: 0 0 0 0.5em;
  }
  .Stories-Item h2 span {
    display: block;
    font-size: 9px;
    text-transform: uppercase;
    color: gray;
  }
  .Stories-Head {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.5em 0 0 0;
  }
  .Stories-Head h2 {
    font-size: 12px;
    font-weight: 600;
  }
  .Stories-Head span {
    font-size: 12px;
    font-weight: normal;
    color: black;
  }
  .Stories-Items {
    margin: 0.5em 0 0.5em 0;
  }
  .Stories-Item-Box {
    width: 32px;
    height: 32px;
    border: double 2px transparent;
    border-radius: 100%;
    background-image: linear-gradient(#fff, #fff),
      radial-gradient(circle at top left, #f09433, #bc1888);
    background-origin: border-box;
    background-clip: content-box, border-box;
  }
</style>
