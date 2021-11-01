<script>
  import successkid from "images/successkid.jpg";
</script>

<svelte:head>
  <meta name="description" content="Blog de live" />

  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:site" content="@test" />
  <meta name="twitter:creator" content="@test" />
  <meta name="twitter:title" content="ejemplos" />
  <meta name="twitter:description" content="Blog de " />
  <meta name="twitter:image" content="https://arepa.s3.amazonaws.com/blogpost-cover.png" />

  <meta name="og:title" content="test" />
  <meta name="og:description" content="Blog de live" />
  <meta name="og:image" content="https://arepa.s3.amazonaws.com/blogpost-cover.png" />
  <meta name="og:url" content="" />
  <meta name="og:site_name" content="test ejemplo" />
  <meta name="og:locale" content="es_CO" />
  <meta name="og:type" content="article" />
  <meta name="fb:app_id" content="" />
  <title>Sapper project template</title>
</svelte:head>

<div class="Home">
  <h1>Blogpost</h1>
</div>

<style>
  h1,
  figure,
  p {
    text-align: center;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  figure {
    margin: 0 0 1em 0;
  }

  img {
    width: 100%;
    max-width: 400px;
    margin: 0 0 1em 0;
  }

  p {
    margin: 1em auto;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>
