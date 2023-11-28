<script setup>
    import {ref} from "vue"    

    const show = ref(true)
</script>

<template>
    <div class="wrapper">
        <button @click="show = !show" class="toggle-button">토글 버튼</button>
        <Transition>
            <p v-if="show" class="toggle-text">위에 버튼 누르면 텍스트 사라짐</p>
        </Transition>
    </div>
</template>

<style scoped>    
    .wrapper  {
        height: 72px;
        text-align: center;
    }
    .toggle-button {
        height: 30px;
        padding: 0 15px;
        margin-bottom: 40px;
        margin-bottom: 10px;
        color: #f1f1f1;
        font-size: 18px;
        border: none;
        border-radius: 15px;
        background: rgb(237, 146, 146);
        cursor: pointer;
        transition: 0.5s;
    }
    .toggle-button:hover {
        background: rgb(178, 178, 241);
    }
    .toggle-text {
        font-size: 20px;
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