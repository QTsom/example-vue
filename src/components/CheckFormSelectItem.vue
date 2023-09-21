<script setup>
    import {ref} from 'vue'

    const selected = ref('')
</script>


<template>
    <div class="wrapper">
        <p class="select-result"><span>"{{ selected }}"</span> 이것이 선택됐슈</p>
        
        <select v-model="selected" class="select-box">
            <option disabled value="">다음 중 하나를 고르시오</option>
            <option>바나나</option>
            <option>사과</option>
            <option>오렌지</option>
        </select>
    </div>
</template>

<style scoped>
    .wrapper {
        display: flex;
        flex-direction: column;
        gap: 20px;
        padding: 20px;
        margin-bottom: 40px;
        background-color: rgb(48, 123, 123);
        border-radius: 10px;
    }
    .wrapper .select-result {
        display: inline-block;
        width: auto;
        font-size: 18px;
        color: rgb(230, 247, 247);
    }
    .wrapper .select-result span {
        font-weight: 700;
    }

    .select-box {
        height: 35px;
        padding: 0 10px;
        border: none;
        border-radius: 5px;
    }
    .select-box:focus-visible {
        border: 2px solid rgb(168, 255, 28);
        outline: none;
    }
</style>