<script setup>
  import Content from "./components/Content.vue"
  import Change from "./components/Change.vue"
  import CountEvent from "./components/CountEvent.vue"
  import MinusCountEvent from "./components/MinusCountEvent.vue"
  import MessageForm from "./components/MessageForm.vue"
  import CheckForm from "./components/CheckForm.vue"
  import Chart from "./components/Chart.vue"
  import BlogPost from "./components/BlogPost.vue"

  const posts = ref([
    {id: 1, title: "첫 번째 리스트"},
    {id: 2, title: "두 번째 리스트"},
    {id: 3, title: "세 번째 리스트"}
  ])

  const postFontColor = ref('000')
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

      <div :style="{ color: '#' + postFontColor }">
        <BlogPos v-for="post in posts" :key="post.id" :title="post.title" @color-text="postFontColor = '888'" />
      </div>
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