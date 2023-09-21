<script setup>
    import {ref} from "vue";

    const minusCounter = ref(0)

    function increment() {
        minusCounter.value--
    }
</script>

<template>
    <div class="wrapper">
        <p class="counter-text">숫자 내려가는 거 한 번 눌러보렴 >> </p>

        <button @click="increment" class="counter-button">
            {{ minusCounter }}
        </button>
    </div>
</template>

<style scoped>
    .wrapper {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        gap: 20px;
        margin-bottom: 20px;
    }
    .counter-button {
        height: 25px;
        padding: 0 20px;
        color: #fff;
        font-size: 18px;
        border: none;
        border-radius: 5px;
        background: #999;
        cursor: pointer;
    }
</style>