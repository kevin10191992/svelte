<script>
  // your script goes here
  export let post;
  import formatIsoTime from "../utils/formatIsoTime.js";
</script>

<!-- markup (zero or more items) goes here -->
<div class="Post-Item">
  <div class="Post-Content">
    <div class="Post-Head">
      <div class="Post-Title">
        <h2>
          <a rel="prefetch" href="blog/{post.slug}">{post.title}</a>
        </h2>
        <p>
          <time datetime={post.createdAt}>📅 {formatIsoTime(post.createdAt)}</time>
          <span class="dot" />
          <span>5 min</span>
        </p>
      </div>
    </div>
    <div class="Post-Tags" />
    <div class="Post-Desc">
      <p>{post.desc}</p>
    </div>
  </div>
</div>

<style>
  .Post-Item {
    color: #191a22;
    position: relative;
  }
  .Post-Content {
    font-size: 16px;
    font-weight: 300;
    display: grid;
    justify-content: space-between;
    grid-gap: 5px;
    grid-template-columns: 1fr;
  }
  .Post-Title {
    font-size: 20px;
    margin: 0;
    padding: 0;
  }
  .Post-Title p {
    color: #333;
    font-size: 13px;
    font-weight: 300;
    margin-top: 5px;
    padding: 0;
  }

  a {
    text-decoration: none;
    color: #22215b;
  }
  .Post-Desc p {
    color: #333;
    font-size: 16px;
    line-height: 28px;
    margin: 0 auto;
    word-break: break-word;
  }
  .dot {
    font-weight: 700;
  }
</style>
