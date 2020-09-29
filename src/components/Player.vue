<template>
  <div class="player">
    <button>Play</button>
    <button>Stop</button>
    <span>Eminem - Lose Yourself</span>
  </div>
</template>

<script>
export default {
  name: 'Player',
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
  }
</style>