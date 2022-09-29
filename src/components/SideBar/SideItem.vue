<script setup lang="ts">
const props = defineProps({
    isActive: {
        type: Boolean,
        default: false
    },
    title: {
        type: String,
        required: true
    }
})
</script>

<template>
    <div class="side-item" :class="{'side-item--active':isActive}">
        <i class="side-item__icon iconfont">&#xe6bd;</i>
        <span class="side-item__title">{{ title }}</span>
    </div>
</template>

<style scoped>
.side-item {
    padding: .5em 1em;
    margin-right: 2em;
    border-radius: 0 2em 2em 0;
    transition: .3s;
    cursor: pointer;
}

.side-item:hover:not(.side-item--active) {
    background-color: #D1D5DB;
}

.side-item--active{
    color: #fff;
    background-color: #EF4444;
}

.side-item__title {
    margin-left: .5em;
    font-size: 1em;
}
</style>