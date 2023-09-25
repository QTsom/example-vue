<script setup>
    import {ref} from "vue"    

    const show = ref(true)
</script>

<template>
    <div class="wrapper">
        <button @click="show = !show" class="toggle-button">토글 버튼</button>
        <Transition>
            <p v-if="show">위에 버튼 누르면 텍스트 사라짐</p>
        </Transition>
    </div>
</template>

<style scoped>    
    .wrapper  {
        text-align: center;
    }
    .toggle-button {
        height: 35px;
        padding: 0 15px;
        margin-bottom: 10px;
        color: #f1f1f1;
        font-size: 20px;
        border: none;
        border-radius: 15px;
        background: rgb(237, 146, 146);
    }
    .v-enter-active,
    .v-leave-active {
    transition: opacity 0.5s ease;
    }

    .v-enter-from,
    .v-leave-to {
    opacity: 0;
    }
</style>