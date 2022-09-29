<script setup lang="ts">
import axios from "axios";
import SlideShow from "./Main/SlideShow.vue";

console.log('hello, world');
axios.get('https://netease-cloud-music-api-livid-seven.vercel.app/search?keywords=%E6%B5%B7%E9%98%94%E5%A4%A9%E7%A9%BA')
    .then(function (response) {
        console.log(response.data);
    })
    .catch(function (error) {
        console.error(error);
    });
</script>

<template>
    <div class="main">
        <SlideShow class="slide-show"></SlideShow>
    </div>
</template>

<style scoped>
    .main{
        background-color: #fff;
    }

    .slide-show{
        width: 100%;
        height: 10em;
    }
</style>