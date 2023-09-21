<script setup>
    defineProps(['title']);
    defineEmits(["color-text"])
</script>

<template>
    <div class="wrapper">
        <h2 class="title">{{ title }}</h2>
        <button @click="$emit('color-text')">뭘 눌러도 텍스트 색상이 한꺼번에 바뀔 것이야</button>
    </div>
</template>

<style scoped>
    .wrapper {
        display: flex;
        justify-content: center;
    }
    .title {
        text-decoration: none;
    }
</style>