<template>
    <div class="wn-content">
        <div class="wn-content__items" v-for="item in 100">{{ item }}</div>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@include b(content) {
    flex: 1;
    overflow: auto;
    @include e(items) {
        padding: 10px;
        margin: 10px;
        border: 1px solid #ccc;
        border-radius: 4px;
    }
}
</style>
