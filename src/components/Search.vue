<template>
  <div class="search">
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
</template>

<script>
export default {
  name: 'Search',
}
</script>

<style>
  .search {
    padding: 20px;
    background: violet;
  }

  .search-field {
    width: 100%;
    font-size: inherit;
    padding: 5px 10px;
  }
</style>