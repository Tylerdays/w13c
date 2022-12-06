<template>
    <div>
        <ul>
            <li v-for="song in songs" :key="song.id">
                {{song.title}} - {{song.artist}}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'SongList',
        data () {
            return{
                songs: [
                    {
                        id: 1,
                        title: 'Temp title1',
                        artist: 'artist1',
                    },
                    {
                        id: 2, 
                        title: 'Temp title2',
                        artist: 'artist2',
                    },
                    {
                        id: 3,
                        title: 'Temp title3',
                        artist: 'artist3',
                    },
                    {
                        id: 4,
                        title: 'Temp title4',
                        artist: 'artist4',
                    },
                    {
                        id: 5,
                        title: 'Temp title5',
                        artist: 'artist5',
                    },
                ]
            }
        },
        methods: {
            //first we have to remove the song from the songlist
            addSongToPlaylist(song) {
                const index = this.songs.findIndex(s => s.id === song.id);
                this.songs.splice(index, 1);
            }
        }
    }
</script>

<style scoped>

</style>