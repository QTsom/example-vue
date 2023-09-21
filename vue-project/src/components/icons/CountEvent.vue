<script setup>
  import {ref} from 'vue'
  
  const count = ref(0)
</script>

<template>
  <div class="wrapper">
    <button @click="count++" class="count-button">
      숫자 올릴 버튼
    </button>

    <p class="count-text">
      숫자 값이 <span class="point">{{ count }}</span> 이렇게 올라감
    </p>
    
    <button @click="count = 0" class="count-button">
      초기화 버튼이야
    </button>
  </div>
  
</template>

<style scoped>
  .wrapper {
    display: flex;
    align-items: baseline;
    justify-content: center;
    gap: 10px;
    margin-bottom: 40px;
  }
  .count-button {
    padding: 0 12px;
    font-size: 16px;
    color: #555;
    line-height: 33px;
    border: none;
    border-radius: 10px;
    background-color: lightblue;
    cursor: pointer;
  }
  .count-text {
    display: flex;
    align-items: baseline;
    gap: 6px;
  }
  .point {
    padding: 5px;
    font-size: 25px;
    color: #ffb703;
    text-emphasis: filled double-circle #ffb703;
  }
</style>