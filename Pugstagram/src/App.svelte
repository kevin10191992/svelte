<script>
  import { onMount } from "svelte";
  import Header from "./Components/Header.svelte";
  import Sidebar from "./Components/Sidebar.svelte";
  import Main from "./Components/Main.svelte";
  import Timeline from "./Components/Timeline.svelte";

  let data = {};
  const API = "https://us-central1-pugstagram-co.cloudfunctions.net/data";
  onMount(async () => {
    const response = await fetch(API);
    data = await response.json();
    // console.log(data);
  });
</script>

<main>
  <Header />
  <Main>
    <Timeline Post={data.posts} />
    <Sidebar {...data.user} />
  </Main>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap");
  @import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");

  :global(.TextPacifico) {
    font-family: "Pacifico", cursive;
  }

  :global(body) {
    /* this will apply to <body> */
    /* your styles go here */
    background-color: #fafafa;
    color: rgba(38, 38, 38, 0.7);
    font-family: "Lato", sans-serif;
    margin: 0;
    padding: 0;
  }

  :global(h1, h2, h3) {
    margin: 0;
    padding: 0;
  }
</style>
