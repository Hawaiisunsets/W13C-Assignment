<template>
    <div>
        <h2>{{songName}}</h2>
        <h3>{{songArtist}}</h3>
        <button @click="addToPlayList">Add to PlayList</button>
    </div>
</template>

<script>
    export default {
        name : "SongList",
        props : {
            songName : String,
            songArtist : String,
            songId : Number
        },
        methods : {
            addToPlayList(){
                this.$emit(`addSong`, this.songName);
            }
        }
    }
</script>

<style scoped>
div{
    border: red 2px solid;
    width: 30vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
}
h2{
    color: blue;
}
h3{
    color: pink;
}
</style>