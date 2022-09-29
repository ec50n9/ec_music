<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps({
    title: String
});

let show = ref(true);

function toggle() {
    show.value = !show.value;
}
</script>

<template>
    <div class="fold-list">
        <div class="title-bar" @click="toggle">
            <span class="title-bar__arrow" :class="{'title-bar__arrow--close': !show}"></span>
            <span class="title-bar__title">{{ title }}</span>
        </div>
        <div class="list" v-show="show">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
.title-bar {
    padding: 1.5em 0 .5em 1em;
    font-size: .8em;
    cursor: pointer;
    user-select: none;
    color: #6B7280;
}

.title-bar__arrow{
    content: '';
    display: inline-block;
    width: 0;
    height: 0;
    border: .4em solid transparent;
    border-top: .4em solid;
    border-bottom: none;
    color: #D1D5DB;
}

.title-bar__arrow--close{
    border: .4em solid transparent;
    border-left: .4em solid;
}

.title-bar__title{
    margin-left: .5em;
}

.fold-list * {
    vertical-align: middle;
}

.list {
    height: auto;
    overflow: hidden;
    transition: 1s;
}
</style>