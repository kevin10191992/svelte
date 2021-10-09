<script>
  // your script goes here
  export let comments = [];
  let ErrorComment = "";

  function AddComment(event) {
    const msg = event.target.Text.value;
    if (msg.length > 3) {
      const comento = {
        id: Date.now(),
        text: msg,
        username: "kperez",
      };

      comments = [...comments, comento];
      event.target.Text.value = "";
      ErrorComment = "";
    } else {
      ErrorComment = "Comentario por lo menos de mas de 3 caracteres ";
    }
  }
</script>

<div class="Comments">
  <div class="Comments-Container">
    <div class="Comments-Users">
      {#each comments as c (c.id)}
        <div class="Commnets-Users-Item">
          <h3>
            {c.username}
          </h3>
          <span>{c.text}</span>
        </div>
      {/each}
    </div>
    <div class="Comments-Add">
      <form on:submit|preventDefault={AddComment}>
        <input
          class="Comments-Input"
          type="text"
          id="Text"
          placeholder="Escribe tu comentario"
        />

        <button type="submit">Post</button>
      </form>
      <small class="ErrorComment">{ErrorComment}</small>
    </div>
  </div>
</div>

<!-- Comments.svelte -->
<style>
  .ErrorComment {
    color: red;
  }
  .Comments h3 {
    font-size: 14px;
    color: black;
    font-weight: bold;
    margin: 0;
    padding: 0;
  }
  .Comments span {
    font-size: 14px;
    margin: 0 0 0 0.5em;
    font-weight: normal;
    color: rgba(black, 0.9);
  }
  .Comments-Add {
    padding: 1em 1em 1em 1em;
    border-top: 1px solid rgba(219, 219, 219, 0.8);
  }
  .Comments-Add form {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .Comments-Container {
    padding: 0 1em 0.5em 1em;
  }
  .Comments-Users {
    margin: 0 0 0.5em 0;
    display: flex;
    flex-direction: column;
  }
  .Commnets-Users-Item {
    margin-bottom: 16px;
  }

  input {
    border: solid 1px #e9e9e9;
    border-radius: 5px;
    color: #696969;
    border: 1px solid transparent;
    font-size: 12px;
    outline: none;
    width: 100%;
    display: flex;
  }
  button {
    border: none;
    color: #3897f0;
    font-size: 12px;
    outline: none;
    cursor: pointer;
    background: none;
  }
</style>
