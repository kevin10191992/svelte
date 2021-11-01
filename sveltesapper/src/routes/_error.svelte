<script>
  export let status;
  export let error;

  const dev = process.env.NODE_ENV === "development";
</script>

<svelte:head>
  <title>{status}</title>
</svelte:head>

<div class="Error404">
  <div class="Error404-Mensaje">
    <h1>{status}</h1>

    <p>{error.message}</p>

    {#if dev && error.stack}
      <pre>{error.stack}</pre>
    {/if}
  </div>
  <div class="Error404-Imagen">
    <figure>
      <img
        src="https://arepa.s3.amazonaws.com/img404.png"
        alt="Error404Imagen"
      />
    </figure>
  </div>
</div>

<style>
  .Error404 {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .Error404-Imagen figure {
    margin: 0;
    padding: 0;
    text-align: right;
  }

  .Error404-Imagen img {
    width: 250px;
    margin: 2em 0 0 0;
    transform: translateY(0px);
    animation: float 8s ease-in-out infinite;
  }

  @keyframes float {
    0% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-40px);
    }
    100% {
      transform: translateY(0px);
    }
  }
</style>
