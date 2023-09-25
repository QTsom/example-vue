<script setup>
  import Content from "./components/Content.vue"
  import Change from "./components/Change.vue"
  import CountEvent from "./components/CountEvent.vue"
  import MinusCountEvent from "./components/MinusCountEvent.vue"
  import MessageForm from "./components/MessageForm.vue"
  import CheckForm from "./components/CheckForm.vue"
  import Chart from "./components/Chart.vue"
  import DoughnutProgress from "./components/DoughnutProgress.vue"
  import TransitionEvent from "./components/TransitionEvent.vue"
</script>

<template>
  <div>
    <h1 class="title">HELLO</h1>
    
    <div>
      <Content />
      
      <Change />
      
      <CountEvent />

      <MinusCountEvent />
      
      <MessageForm />
      
      <CheckForm />

      <Chart />

      <DoughnutProgress />

      <TransitionEvent />
    </div>
  </div>
</template>

<style scope>
  .title {
    font-size: 30px;
    font-weight: 800;
    text-align: center;
    text-decoration: underline;
  }
</style>