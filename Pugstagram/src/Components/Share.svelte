<script>
</script>

<div class="Share">
  <div class="Share-Head">
    <h2>Compartir</h2>
    <span on:click>
      <i class="fas fa-times-circle" />
    </span>
  </div>
  <div class="Share-Container">
    <a
      href="https://www.facebook.com/sharer/sharer.php?&u=https://pugstagram.co"
      target="_blank"
    >
      <span>
        <i class="fab fa-facebook-square" />
      </span>Compartir en Facebook
    </a>
  </div>
</div>

<style>
  .Share {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;
    width: 300px;
    height: 80px;
    position: absolute;
    top: 300px;
    left: 30%;
    z-index: 9;
    padding: 1em;
  }
  .Share-Head {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .Share-Head h2 {
    font-size: 16px;
  }
  .Share-Head span {
    cursor: pointer;
  }
  .Share-Container a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: black;
    font-size: 14px;
    margin: 2em 0 0 0;
  }
  .Share-Container span {
    color: #3b5998;
    margin: 0 0.5em 0 0;
    font-size: 20px;
  }
</style>
