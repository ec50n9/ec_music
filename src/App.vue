<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Header from './components/Header.vue';
import SideBar from './components/SideBar.vue';
import Main from './components/Main.vue';
import PlayBar from './components/PlayBar.vue';
</script>

<template>
  <Header id="header"></Header>
  <div class="main-wrapper">
    <SideBar id="side_bar"></SideBar>
    <Main id="main"></Main>
  </div>
  <PlayBar id="play_bar"></PlayBar>
</template>

<style>
@font-face {
  font-family: 'iconfont';
  /* Project id 3120812 */
  src: url('//at.alicdn.com/t/font_3120812_3f39iu0mx29.woff2?t=1650358188571') format('woff2'),
    url('//at.alicdn.com/t/font_3120812_3f39iu0mx29.woff?t=1650358188571') format('woff'),
    url('//at.alicdn.com/t/font_3120812_3f39iu0mx29.ttf?t=1650358188571') format('truetype');
}

.iconfont {
  font-family: "iconfont" !important;
  font-size: 1.5em;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -webkit-text-stroke-width: 0.2px;
  -moz-osx-font-smoothing: grayscale;
}

html,
body,
#app {
  width: 100%;
  height: 100%;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#header {
  width: 100%;
  height: 4em;
}

.main-wrapper {
  display: flex;
  flex-direction: row;
  height: calc(100% - 8em);
}

#side_bar {
  width: 30%;
  max-width: 20em;
}

#main {
  flex-grow: 1;
}

#play_bar {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 4em;
}
</style>
