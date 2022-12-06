<template>
    <div>
        <h1>Pick a song and add it to your playlist.</h1>
        <SongList
            v-for="(song, index) in songs"
            :key="index"
            :songName="song.name"
            :songArtist="song.artist"
            :songId="song.id"
            />
        <PlayList/>
    </div>
</template>

<script>
import SongList from "@/components/SongList.vue";
import PlayList from "@/components/PlayList.vue";   
    export default {
        name : "PageBody",
        components : {
            SongList,
            PlayList
        },
        data () {
            return {
                isSelected : false,
                songs : [
                    {
                        id : 0,
                        name : "Anti-Hero",
                        artist : "Taylor Swift"
                    },
                    {
                        id : 1,
                        name : "Rich Flex",
                        artist : "Drake & 21 Savage"
                    },
                    {
                        id : 2,
                        name : "Unholy",
                        artist : "Sam Smith & Kim Petras"
                    },
                    {
                        id : 3,
                        name : "Bad Habit",
                        artist : "Steve Lacy"
                    },
                    {
                        id : 4,
                        name : "All I Want For Christmas Is You",
                        artist : "Mariah Carey",
                    },
                    {
                        id : 5,
                        name : "Rockin Around The Christmas Tree",
                        artist : "Brenda Lee"
                    },
                    {
                        id : 6,
                        name : "I'm Good",
                        artist : "David Guetta & Bebe Rexha"
                    },
                ]
            }
        },
        // methods : {
        //     showSongs(){
        //         for (let getSongs of this.songs){
        //             // console.log(getSongs);
        //             document.querySelector(`div`).insertAdjacentHTML(`beforeend`, `<p>${getSongs.id}</p>`);
        //             document.querySelector(`div`).insertAdjacentHTML(`beforeend`, `<p>${getSongs.name}</p>`);
        //             document.querySelector(`div`).insertAdjacentHTML(`beforeend`, `<p>${getSongs.artist}</p>`);
        //         }
        //     },
        // },
        // mounted(){
        //     this.showSongs();
        // },
    }
</script>

<style scoped>

</style>