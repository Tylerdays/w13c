<template>
  <div id="app">
    <SongList :songs="songs" @add-song="onAddSong"/>
    <PlayList :songs="PlayList" @remove-song="onRemoveSong"/>
  </div>

</template>

<script>
import SongList from './components/SongList.vue'
import PlayList from './components/PlayList.vue'

export default {
  name: 'App',
  components: {
    SongList,
    PlayList,
  },
  data (){
    return {
      songs: [],
      PlayList: []
    }
  },
  methods: {
    onAddSong(song) {
      this.PlayList.push(song);
    },
    onRemove(song) {
      this.songs.push(song);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
