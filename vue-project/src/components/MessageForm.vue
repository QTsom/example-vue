<script setup>
    import {ref} from 'vue'
    
    const message = ref('')
</script>

<template>
    <div class="wrapper">
        <input v-model="message" placeholder="메세지 입력하기" class="input-box" />
        <p class="message-box"> <span>메시지 내용 :</span> "{{message}}"</p>
    </div>
</template>

<style scoped>
    .wrapper {
        padding: 20px;
        margin-bottom: 40px;
        border-radius: 10px;
        background-color: wheat;
    }
    .input-box {
        width: 100%;
        height: 40px;
        padding: 0 20px;
        margin-bottom: 20px;
        font-size: 14px;
        font-weight: 600;
        border: none;
        color: rgb(181, 118, 0);
        border-radius: 4px;
        caret-color: rgb(181, 118, 0);
        background: rgb(252, 242, 223);
    }
    .input-box::placeholder {
        font-weight: 400;
        color: rgb(181, 118, 0);
    }
    .input-box:focus {
        outline: none;
        border: 1px solid rgb(181, 118, 0);
    }
    .message-box {
        font-size: 18px;
        font-weight: 700;
        color: rgb(181, 118, 0);
    }
    .message-box span {
        font-size: 16px;
        font-weight: 400;
    }
</style>