<script>
  export let segment;
</script>

<nav class="Nav">
  <div class="Nav-Container">
    <div class="Nav-Content">
      <ul>
        <li>
          <a aria-current={segment === undefined ? "page" : undefined} href="."
            >home</a
          >
        </li>
        <li>
          <a
            aria-current={segment === "about" ? "page" : undefined}
            href="about">about</a
          >
        </li>
        <li>
          <a
            aria-current={segment === "contact" ? "page" : undefined}
            href="contact">contact</a
          >
        </li>
        <li>
          <a
            aria-current={segment === "general" ? "page" : undefined}
            href="general">general</a
          >
        </li>

        <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
						 the blog data when we hover over the link or tap it on a touchscreen -->
        <li>
          <a
            rel="prefetch"
            aria-current={segment === "blog" ? "page" : undefined}
            href="blog">blog</a
          >
        </li>
      </ul>
    </div>
    <div class="Nav-Social" />
  </div>
</nav>

<style>
  .Nav {
    border-bottom: 1px solid rgb(255, 0, 121, 0.2);
    font-weight: 300;
    background-color: #fafbfc;
    color: #191a22;
  }

  .Nav-Container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }

  .Nav-Content {
    display: flex;
    justify-content: space-between;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: block;
    float: left;
  }

  [aria-current] {
    position: relative;
    display: inline-block;
	font-weight: bold;
    color: black;
  }

  [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: rgb(255, 62, 0);
    display: block;
    bottom: -1px;
  }

  a {
    text-decoration: none;
    padding: 1em 1em 1em 0;
    display: block;
    font-size: 14px;
    font-weight: 300;
    transition: all 0.3s ease-in-out 0s;
    color: rgb(25, 26, 34, 0.57);
  }
  a:hover {
    color: rgb(25, 26, 34, 1);
    font-weight: bold;
  }
</style>
