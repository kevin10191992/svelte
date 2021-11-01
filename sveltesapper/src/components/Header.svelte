<script>
  // your script goes here
</script>

<header class="Header">
  <div class="Header-Container">
    <div class="Header-Content">
      <div class="Header-Logo">
        <h1>Kevin Perez</h1>
        <span>FrontEnd Example</span>
      </div>
      <div class="Header-Social">
        <ul>
          <li>
            <a href="/" target="_blank" rel="noreferer">
              <img src="github-icon.png" alt="github-icon" />
            </a>
          </li>
          <li>
            <a href="/" target="_blank" rel="noreferer">
              <img src="facebook-icon.png" alt="facebook-icon" />
            </a>
          </li>
          <li>
            <a href="/" target="_blank" rel="noreferer">
              <img src="instagram-icon.png" alt="instagram-icon" />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</header>

<!-- markup (zero or more items) goes here -->
<style>
  /* your styles go here */
  .Header {
    background-color: #fafbfc;
    color: #191a10;
    padding: 1em 0 0 0;
  }

  .Header-Container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }

  .Header-Content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .Header h1 {
    color: #191a22;
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 0.8px;
    cursor: pointer;
  }

  .Header h1 span {
    display: block;
    font-size: 13px;
    font-weight: 300;
    letter-spacing: normal;
    margin: 0.3em 0 0 0;
  }

  .Header ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .Header li {
    display: inline-block;
    margin: 0 0.5em 0 0;
  }

  .Header a {
    text-decoration: none;
    font-weight: 300;
    font-size: 14px;
  }

  .Header-Social img {
    width: 20px;
  }
</style>
