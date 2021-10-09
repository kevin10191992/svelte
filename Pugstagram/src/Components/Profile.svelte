<script>
  // your script goes here
  export let nickname = "";
  export let name = "";
</script>

<div class="Profile">
  <div class="Profile-Container">
    <div class="Profile-Avatar">
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar" />
    </div>
    <div class="Profile-Info">
      <h2>{nickname}</h2>
      <span>{name}</span>
    </div>
  </div>
</div>

<!-- Profile.svelte -->
<style>
  .Profile-Container {
    display: flex;
    align-items: center;
  }
  .Profile-Avatar img {
    width: 42px;
    height: 42px;
    border-radius: 50%;
  }
  .Profile-Info {
    margin: 0 0 0 0.5em;
  }
  .Profile-Info h2 {
    font-size: 14px;
    color: black;
    margin: 0;
    padding: 0;
  }
  .Profile-Info span {
    font-size: 12px;
    font-weight: normal;
  }
</style>
