<script setup lang="ts">
let song = {
    name: '海阔天空',
    author: 'Beyoung'
}
</script>

<template>
    <div class="play-bar">
        <progress class="progress" value="40" max="100"></progress>
        <img class="cover" src="../assets/logo.png" alt="cover">
        <div class="song-info">
            <div class="song-info__text">
                <span class="song-info__name">{{song.name}}</span>
                <span class="song-info__author">{{song.author}}</span>
            </div>
            <div class="song-info__time">00:29 / 02:53</div>
        </div>
        <div class="controller">
            <i class="controller__like iconfont">&#xe63d;</i>
            <i class="controller__previous iconfont">&#xe6c0;</i>
            <i class="controller__play iconfont">&#xe6af;</i>
            <i class="controller__next iconfont">&#xe6ae;</i>
            <i class="controller__share iconfont">&#xe6bb;</i>
        </div>
        <div class="function">
            <i class="function__loop iconfont">&#xe6bf;</i>
            <i class="function__play-list iconfont">&#xe6c2;</i>
            <i class="function__sound iconfont">&#xe6b2;</i>
        </div>
    </div>
</template>

<style scoped>
.play-bar {
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: #fff;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.progress{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
    border: none;
    border-radius: 0;
    color: #EF4444;
    background-color: #F3F4F6;
}

.progress::-moz-progress-bar{
    background-color: #EF4444;
}

.cover {
    width: 3em;
    height: 3em;
    margin: .5em;
    object-fit: contain;
    border-radius: .5em;
}

.song-info{
    max-width: 40%;
    text-align: left;
}

.song-info__text *{
    vertical-align: middle;
}

.song-info__name{
    font-size: 1em;
}

.song-info__author{
    color: #6B7280;
    font-size: .8em;
}

.song-info__author::before {
    content: ' - ';
}

.song-info__time{
    color: #6B7280;
    font-size: .8em;
}

.controller{
    flex-grow: 1;
    text-align: center;
}

.controller *{
    margin: 0 .5em;
}

.controller__previous, .controller__next{
    color: #EF4444;
}

.controller__like, .controller__share{
    color: #6B7280;
}

.controller__play{
    padding: .5em;
    color: #fff;
    background-color: #EF4444;
    border-radius: 50%;
}

.function *{
    margin: 0 .5em;
    color: #6B7280;
}

</style>