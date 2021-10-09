<script>
  //
  import Comments from "./Comments.svelte";
  import Modal from "./Modal.svelte";
  import Share from "./Share.svelte";
  import { blur } from "svelte/transition";
  import { LikeCount } from "../Store/Store";

  //export
  export let username;
  export let location;
  export let photo;
  export let postComment;
  export let comments = [];
  export let avatar;

  let isModal = false;
  let like = false;
  let bookmark = false;
  //
  function ClickLike() {
    like = like ? false : true;
    if (like) {
      LikeCount.update((v) => v + 1);
    } else {
      LikeCount.update((v) => v - 1);
    }
  }

  function ClickBookmark() {
    bookmark = bookmark ? false : true;
  }

  function ClickModal() {
    isModal = isModal ? false : true;
  }
</script>

<div class="Card">
  {#if isModal}
    <div transition:blur>
      <Modal>
        <Share on:click={ClickModal} />
      </Modal>
    </div>
  {/if}

  <div class="Card-Container">
    <div class="Card-Header">
      <div class="Card-User">
        <img src={avatar} alt={username} />
        <h2>
          {username}
          <span>{location}</span>
        </h2>
      </div>

      <div class="Card-Settings">
        <span>
          <i class="fa fa-ellipsis-h" aria-hidden="true" />
        </span>
      </div>
    </div>

    <div class="Card-Photo">
      <figure on:dblclick={ClickLike}>
        <img src={photo} alt={username} />
      </figure>
    </div>

    <div class="Card-Icons">
      <div class="Card-Icons-First">
        <span on:click={ClickLike} class:active-Like={like}>
          <i class="fas fa-heart" />
        </span>
        <span on:click={ClickModal}>
          <i class="fas fa-paper-plane" />
        </span>
      </div>

      <div class="Card-Icons-Second" class:active-Bookmark={bookmark}>
        <span on:click={ClickBookmark}>
          <i class="fas fa-bookmark" />
        </span>
      </div>
    </div>

    <div class="Card-Description">
      <h3>{username}</h3>
      <span>{postComment}</span>
    </div>

    <Comments {comments} />
  </div>
</div>

<!-- Card.svelte -->
<style>
  .Card {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;
  }
  .Card-Header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1em;
  }
  .Card-User {
    display: flex;
    align-items: center;
    justify-content: flex-end;
  }
  .Card-User img {
    width: 32px;
    height: 32px;
    border-radius: 50%;
  }
  .Card-User h2 {
    margin: 0;
    padding: 0;
    font-size: 14px;
    font-weight: 600;
    margin: 0 0 0 1em;
    color: black;
  }
  .Card-User h2 span {
    display: block;
    font-size: 12px;
    font-weight: normal;
    color: rgba(38, 38, 38, 0.7);
  }
  .Card-Photo {
    padding: 0;
    margin: 0;
  }
  .Card-Photo img {
    width: 100%;
    height: auto;
  }
  .Card-Photo figure {
    margin: 0;
    padding: 0;
    cursor: pointer;
  }
  .Card-Settings i {
    cursor: pointer;
  }
  .Card-Icons {
    padding: 1em;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .Card-Icons span {
    margin: 0 1em 0 0;
    cursor: pointer;
    font-size: 20px;
  }
  .Card-Icons i:last-child {
    margin: 0;
  }
  .Card-Description {
    padding: 0 1em 1em 1em;
  }
  .Card-Description h3 {
    font-size: 14px;
    font-weight: bold;
    color: black;
  }
  .Card-Description span {
    font-size: 14px;
  }

  .active-Like {
    color: #bc1888;
    animation: bounces linear 0.8s;
    animation-iteration-count: 1;
    transform-origin: 20% 20%;
  }

  .active-Bookmark {
    color: #f09433;
  }

  @keyframes bounces {
    0% {
      transform: translate(0px, 0px);
    }
    15% {
      transform: translate(0px, -25px);
    }
    30% {
      transform: translate(0px, 0px);
    }
    45% {
      transform: translate(0px, -15px);
    }
    60% {
      transform: translate(0px, 0px);
    }
    75% {
      transform: translate(0px, -5px);
    }
    100% {
      transform: translate(0px, 0px);
    }
  }
</style>
