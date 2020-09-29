<template>
  <div class="player">
    <button @click="$emit('play')">Play</button>
    <button @click="$emit('stop')">Stop</button>
    <span>{{ trackDescription }}</span>
  </div>
</template>

<script>
export default {
  name: 'Player',
  props: {
    track: Object,
  },
  computed: {
    trackDescription () {
      const parts = [this.track.artist, this.track.title]

      return parts.filter(Boolean).join(' - ')
    }
  }
}
</script>

<style>
  .player {
    padding: 20px;
    background: indianred;
  }

  .player button {
    margin-right: 20px;
    font-size: inherit;
    /* height: 30px; */
  }
  /* .player .track-description {
    d
  } */
</style>