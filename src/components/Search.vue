<template>
  <div class="search">
    <input
      class="search-field"
      type="text"
      @keyup.enter="search($event.target.value)"
    >
    
    <div
      v-for="track in tracks"
      :key="track.id"
      class="track"
    >
      <div class="description">{{ track.artist }} - {{ track.title }}</div>
      <div>
        <button>Add</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Search',
  data () {
    return {
      tracks: [],
    }
  },
  methods: {
    search (value) {
      this.tracks = [
        {
          id: 1109731,
          title: 'Lose Yourself',
          preview: 'https://cdns-preview-1.dzcdn.net/stream/c-13039fed16a173733f227b0bec631034-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 916424,
          title: 'Without Me',
          preview: 'https://cdns-preview-c.dzcdn.net/stream/c-cca63b2c92773d54e61c5b4d17695bd2-8.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109737,
          title: 'The Real Slim Shady',
          preview: 'https://cdns-preview-d.dzcdn.net/stream/c-d28ee67c24d60e740866c7709d772f55-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 6461432,
          title: 'Not Afraid',
          preview: 'https://cdns-preview-0.dzcdn.net/stream/c-04c2c479846725eec24a3f40e837d35e-16.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109739,
          title: 'Mockingbird',
          preview: 'https://cdns-preview-6.dzcdn.net/stream/c-655dfb802c35579d26a32136e3d0e7b3-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 72160314,
          title: 'Rap God',
          preview: 'https://cdns-preview-2.dzcdn.net/stream/c-2a2a808c0966c0952aa4f6bae6fa98de-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 548348732,
          title: 'Venom',
          preview: 'https://cdns-preview-8.dzcdn.net/stream/c-8ad574e54c315bd9f89ba34deb2c7650-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109729,
          title: 'My Name Is',
          preview: 'https://cdns-preview-b.dzcdn.net/stream/c-b410ccaf3c000eeaa74025f558892638-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109744,
          title: 'When I\'m Gone',
          preview: 'https://cdns-preview-8.dzcdn.net/stream/c-8aaafada99fb0a10485ea594f664d917-13.mp3',
          artist: 'Eminem'
        },
        {
          id: 916414,
          title: 'Cleanin\' Out My Closet',
          preview: 'https://cdns-preview-f.dzcdn.net/stream/c-f052966abff92ac3ca9e29fbe62b50eb-8.mp3',
          artist: 'Eminem'
        },
        {
          id: 854914332,
          title: 'Darkness',
          preview: 'https://cdns-preview-2.dzcdn.net/stream/c-243c0a920bc2c41b18bcd8a20ca5ee41-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 916426,
          title: 'Sing For The Moment',
          preview: 'https://cdns-preview-6.dzcdn.net/stream/c-6a0f240c7bd580e87697146ed3247ab5-8.mp3',
          artist: 'Eminem'
        },
        {
          id: 556305252,
          title: 'Killshot',
          preview: 'https://cdns-preview-3.dzcdn.net/stream/c-3be8a7e6ae1b8c6ba30a81bd3525a4b2-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109727,
          title: 'The Way I Am',
          preview: 'https://cdns-preview-6.dzcdn.net/stream/c-648abd8c64b8452a703bf48139b0ba64-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 555640142,
          title: 'Venom',
          preview: 'https://cdns-preview-c.dzcdn.net/stream/c-c2f1132eab78414f78402c5f3dd35f5b-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 548348702,
          title: 'Fall',
          preview: 'https://cdns-preview-6.dzcdn.net/stream/c-651d9d92840db585ff2ec2651dc464d8-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 548348612,
          title: 'The Ringer',
          preview: 'https://cdns-preview-8.dzcdn.net/stream/c-825009c6222c3c827f0d1da6dd8a2ae0-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 916445,
          title: '\'Till I Collapse',
          preview: 'https://cdns-preview-1.dzcdn.net/stream/c-12eca10f7e8e55f7f83c14b3552f1940-9.mp3',
          artist: 'Eminem'
        },
        {
          id: 3729755,
          title: 'Beautiful',
          preview: 'https://cdns-preview-e.dzcdn.net/stream/c-e92465651c31a0e9d61467de54e1aa35-11.mp3',
          artist: 'Eminem'
        },
        {
          id: 548348692,
          title: 'Kamikaze',
          preview: 'https://cdns-preview-c.dzcdn.net/stream/c-c805ad156a2754311cb7ba8faa38d7f7-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109736,
          title: 'Like Toy Soldiers',
          preview: 'https://cdns-preview-9.dzcdn.net/stream/c-95323b6fa73fee831fef54ede332e4ab-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 1109743,
          title: 'Just Lose It',
          preview: 'https://cdns-preview-3.dzcdn.net/stream/c-3b0ff89db077f237f9c405dc4afaa1e2-12.mp3',
          artist: 'Eminem'
        },
        {
          id: 854914262,
          title: 'Premonition',
          preview: 'https://cdns-preview-d.dzcdn.net/stream/c-de98e71ba0560593f855a280e96565ec-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 72160313,
          title: 'Berzerk',
          preview: 'https://cdns-preview-d.dzcdn.net/stream/c-dff067bd0d45ccf376840638c10ee38b-6.mp3',
          artist: 'Eminem'
        },
        {
          id: 71607569,
          title: 'Rap God',
          preview: 'https://cdns-preview-4.dzcdn.net/stream/c-420ce81664ab21b903144a62be7979f0-7.mp3',
          artist: 'Eminem'
        }
      ] 

      // fetch(`https://deezerdevs-deezer.p.rapidapi.com/search?q=${value}`, {
      //   "method": "GET",
      //   "headers": {
      //     "x-rapidapi-host": "deezerdevs-deezer.p.rapidapi.com",
      //     "x-rapidapi-key": "65be59086emsh24aaa53bfa31632p119927jsn7cb335faef8b"
      //   }
      // })
      // .then(response => response.json())
      // .then(data => {
      //   this.tracks = data.data.map(el => ({
      //     id: el.id,
      //     title: el.title_short,
      //     preview: el.preview,
      //     artist: el.artist.name
      //   }))
      // })
      // .catch(err => {
      //   console.log(err);
      // });
    }
  }
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