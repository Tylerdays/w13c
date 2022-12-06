<template>
    <div>
        <h2>PlayList</h2>
        <ul>
            <li v-for="song in songs" :key="song.id">
            {{song.title}} - {{song.artist}}
            <button @click="removeSongFromPlayList(song)">Remove From PlayList</button>
        </li>
            
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'PlayList',
        data () {
            return {
                songs: []
            }
        },
        methods: {
            removeSongFromPlayList(song) {
                // Removing the song from PlayList
                const index = this.songs.findIndex(s => s.id === song.id);
                this.songs.splice(index, 1);

                // Adding the song back to the songlist
                this.$emit('remove-song', song);
        }
        }
    }
</script>

<style scoped>

</style>