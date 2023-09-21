<script setup>
    import {ref} from 'vue'

    const picked = ref('')
</script>


<template>
    <div class="wrapper">
        <p>선택한 거 : <span class="picked-item">" {{ picked }} "</span></p>

        <div class="radio-list">
            <div class="radio-item">
                <input type="radio" name="radioPick" id="first" value="first" v-model="picked">
                <label for="first">first</label>
            </div>
            <div class="radio-item">
                <input type="radio" name="radioPick" id="second" value="second" v-model="picked">
                <label for="second">second</label>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .wrapper {
        padding: 20px;
        margin-bottom: 40px;
        border-radius: 10px;
        background-color: rgb(219, 189, 246);
    }
    .wrapper > p {
        margin-bottom: 10px;
    }
    .wrapper .picked-item {
        color: rgb(107, 0, 207);
    }

    .radio-list {
        padding-left: 30px;
    }
    .radio-item input {
        display: none;
    }
    .radio-item input + label {
        display: flex;
        align-items: center;
        gap: 10px;
        cursor: pointer;
    }
    .radio-item input + label::before {
        content: "";
        width: 15px;
        height: 15px;
        border: 1px solid #000;
        border-radius: 50%;
    }
    .radio-item input:checked + label::before {
        background: #000;
    }
</style>