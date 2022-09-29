<script setup lang="ts">
import SideItem from './SideBar/SideItem.vue';
import FoldList from './SideBar/FoldList.vue';

</script>

<template>
    <div class="side-bar">
        <div class="profile">
            <img class="profile__img" src="../assets/logo.png" alt="profile">
            <span class="profile__name">ShelloWorld</span>
        </div>
        <SideItem title="我喜欢的音乐"></SideItem>
        <SideItem title="本地音乐"></SideItem>
        <SideItem title="垃圾桶"></SideItem>
        <FoldList title="创建的歌单">
            <SideItem title="我喜欢的音乐"></SideItem>
            <SideItem :isActive="true" title="本地音乐"></SideItem>
            <SideItem title="垃圾桶"></SideItem>
        </FoldList>
        <FoldList title="创建的歌单">
            <SideItem title="我喜欢的音乐"></SideItem>
            <SideItem title="本地音乐"></SideItem>
            <SideItem title="垃圾桶"></SideItem>
        </FoldList>
    </div>
</template>

<style scoped>
.side-bar {
    overflow-y: scroll;
    background-color: #fff;
}

.profile {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.profile__img {
    width: 3em;
    height: 3em;
    border-radius: 50%;
    margin: .5em;
}

.profile__name {
    font-size: 1em;
    font-weight: 700;
}
</style>