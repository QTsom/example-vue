<script setup>
  import {ref} from 'vue'
  
  const awesome = ref(true)
</script>

<template>
  <div class="wrapper">
    <p v-if="awesome">
      -- 버튼 누르기 전 --
    </p>
    <p v-else class="last-text">
      -- 버튼 누른 후 --
    </p>
    
    <button @click="awesome = !awesome" class="click-button">
        문구 바꾸기
    </button>

  </div>
</template>

<style scoped>
  .wrapper {
    margin: 40px 0;
    text-align: center;
  }
  .wrapper p {
    margin: 10px 0;
  }
  .click-button {
    line-height: 30px;
    padding: 0 15px;
    font-size: 16px;
    color: #555;
    background-color: lightgreen;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
  .last-text {
    font-size: 18px;
    color: green;
  }
</style>