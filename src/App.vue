<template>
  <div id="app">
    <Player
      :track="currentTrack"
      @play="playTrack"
      @stop="stopTrack"
    />
    <div class="main">
      <Playlist
        class="main-playlist"
        :tracks="tracks"
        @play="playNewTrack"
        @remove="removeTrack"
      />
      <Search
        class="main-search"
        @add="addTrack"
      />
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
  },
  data () {
    return {
      tracks: [],
      currentTrack: {},
      audio: new Audio(),
    }
  },
  methods: {
    addTrack (newTrack) {
      const amount = this.tracks
        .filter(track => track.id === newTrack.id)
        .length

      this.tracks.push({
        ...newTrack,
        playlistId: newTrack.id + '_' + (amount + 1)
      })
    },
    removeTrack (index) {
      this.tracks.splice(index, 1)
    },
    playNewTrack (index) {
      this.audio.pause()
      
      if (index < 0 || index >= this.tracks.length) {
        return
      }

      this.currentTrack = this.tracks[index]
      this.audio = new Audio(this.currentTrack.preview)
      this.audio.play()
      this.audio.volume = 0.1
      this.audio.onended = () => {
        this.playNewTrack(index + 1)
      }
    },
    playTrack () {
      if (!this.currentTrack.preview) {
        this.playNewTrack(0)
        return
      }
      this.audio.play()
    },
    stopTrack () {
      this.audio.pause()
      this.audio.currentTime = 0
    },
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
</style>
