<template>
  <div class="playlist">
    <Track
      v-for="(track, index) in tracks"
      :key="track.playlistId"
      :artist="track.artist"
      :title="track.title"
      :track-from-playlist="true"
      @play="$emit('play', index)"
      @remove="$emit('remove', index)"
    />
  </div>
</template>

<script>
import Track from './Track'

export default {
  name: 'Playlist',
  components: {
    Track,
  },
  props: {
    tracks: Array,
  },
}
</script>

<style>
  .playlist {
    padding: 20px;
    background: greenyellow;
  }

  .playlist .track:first-child {
    margin-top: 0;
  }
</style>