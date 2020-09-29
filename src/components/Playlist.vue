<template>
  <div class="playlist">
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
</template>

<script>
export default {
  name: 'Playlist',
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