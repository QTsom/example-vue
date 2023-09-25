<script setup>
    import {ref} from "vue"    

    const show = ref(true)
</script>

<template>
    <div>
        <button @click="show = !show">토글 버튼</button>
        <Transition>
            <p v-if="show">안녕</p>
        </Transition>
    </div>
</template>

<style scoped>    
    .v-enter-active,
    .v-leave-active {
    transition: opacity 0.5s ease;
    }

    .v-enter-from,
    .v-leave-to {
    opacity: 0;
    }
</style>