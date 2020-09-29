<template>
  <div class="track">
    <div class="description">{{ artist }} - {{ title }}</div>
    <div v-if="trackFromPlaylist">
      <button @click="$emit('play')">Play</button>
      <button @click="$emit('remove')">Remove</button>
    </div>
    <div v-else>
      <button @click="$emit('add')">Add</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Track',
  props: {
    artist: String,
    title: String,
    trackFromPlaylist: Boolean,
  }
}
</script>

<style>
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