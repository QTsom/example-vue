<template>
    <div class="wrapper">
        <Bar :data="data" :options="options" />
    </div>
</template>

<script lang="ts">
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  BarElement,
  CategoryScale,
  LinearScale
} from 'chart.js'
import { Bar } from 'vue-chartjs'
import * as chartConfig from './chartConfig.js'

ChartJS.register(CategoryScale, LinearScale, BarElement, Title, Tooltip)

export default {
  name: 'App',
  components: {
    Bar
  },
  data() {
    return chartConfig
  }
}
</script>

<style scoped>
    .wrapper {
        height: 250px;
        padding-bottom: 40px;
        margin-bottom: 60px;
        border-bottom: 1px solid #888;
    }
</style>