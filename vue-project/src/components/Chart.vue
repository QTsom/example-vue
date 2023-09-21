<template>
    <div class="wrapper">
        <Bar :data="data" :options="options" />
    </div>
</template>

<script lang="ts">
import {
  Chart as ChartJS,
  Title,
  Legend,
  Tooltip,
  BarElement,
  CategoryScale,
  LinearScale
} from 'chart.js'
import { Bar } from 'vue-chartjs'
import * as chartConfig from './chartConfig.js'

ChartJS.register(CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend)

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
        height: 200px;
        margin-bottom: 50px;
    }
</style>