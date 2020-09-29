<template>
  <div id="app">
    <div class="player">
      <button>Play</button>
      <button>Stop</button>
      <span>Eminem - Lose Yourself</span>
    </div>
    <div class="main">
      <div class="main-playlist playlist">
        <div class="track">
          <div class="description">Eminem - Lose Yourself</div>
          <div>
            <button>Play</button>
            <button>Remove</button>
          </div>
        </div>
        <div class="track">
          <div class="description">Eminem - Not Afraid</div>
          <div>
            <button>Play</button>
            <button>Remove</button>
          </div>
        </div>
        <div class="track">
          <div class="description">Eminem - Mockingbird</div>
          <div>
            <button>Play</button>
            <button>Remove</button>
          </div>
        </div>
      </div>
      <div class="main-search search">
        <input
          class="search-field"
          type="text"
        >
        <div class="track">
          <div class="description">Eminem - Lose Yourself</div>
          <div>
            <button>Add</button>
          </div>
        </div>
        <div class="track">
          <div class="description">Eminem - Without Me</div>
          <div>
            <button>Add</button>
          </div>
        </div>
        <div class="track">
          <div class="description">Eminem - The Real Slim Shady</div>
          <div>
            <button>Add</button>
          </div>
        </div>
        <div class="track">
          <div class="description">Eminem - Not Afraid</div>
          <div>
            <button>Add</button>
          </div>
        </div>
        <div class="track">
          <div class="description">Eminem - Mockingbird</div>
          <div>
            <button>Add</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0;
  }
  #app {
    width: 70%;
    margin: 0 auto;
    font-size: 20px;
    font-family: Arial, Helvetica, sans-serif;
  }
  .main {
    display: flex;
  }
  .main-playlist {
    flex: 1 1 0;
    min-height: calc(100vh - 70px);
  }
  .main-search {
    flex: 1 1 0;
  }

  .player {
    padding: 20px;
    background: indianred;
  }

  .player button {
    margin-right: 20px;
    font-size: inherit;
  }

  .playlist {
    padding: 20px;
    background: greenyellow;
  }

  .playlist .track:first-child {
    margin-top: 0;
  }

  .search {
    padding: 20px;
    background: violet;
  }

  .search-field {
    width: 100%;
    font-size: inherit;
    padding: 5px 10px;
  }

  .track {
    display: flex;
    margin: 10px 0;

    font-size: 16px;

    color: white;
    background:cornflowerblue;
  }
  .track .description {
    flex: 1 1 auto;
  }
  .track button {
    margin-left: 10px;
  }
</style>
