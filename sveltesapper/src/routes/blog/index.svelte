<script context="module">
  export function preload() {
    return this.fetch(`blog.json`)
      .then((r) => r.json())
      .then((posts) => {
        return { posts };
      });
  }
</script>

<script>
  import Post from "../../components/Post.svelte";
  export let posts;
</script>

<svelte:head>
  <title>Kevin Perez</title>
</svelte:head>

<h1>Recent posts</h1>

<ul>
  {#each posts as post}
    <Post {post} />
  {/each}
</ul>

<style>
  
</style>
