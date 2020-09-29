<template>
  <div id="app">
    <Player />
    <div class="main">
      <Playlist class="main-playlist" />
      <Search class="main-search" />
    </div>
  </div>
</template>

<script>
import Player from './components/Player'
import Playlist from './components/Playlist'
import Search from './components/Search'

export default {
  name: 'App',
  components: {
    Player,
    Playlist,
    Search,
  }
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
