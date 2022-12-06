<template>
    <div>
        <ul>
            <li v-for="song in songs" :key="song.id">
            {{song.title}} - {{song.artist}}</li>
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
        }
    }
</script>

<style scoped>

</style>