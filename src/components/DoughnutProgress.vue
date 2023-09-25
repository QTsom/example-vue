<template>
    <div class="wrapper">    
        <Doughnut :data="data" :options="options" />
    </div>
</template>

<script lang="ts">
    import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
    import { Doughnut } from 'vue-chartjs'
    import * as progressConfig from './progressConfig.js'

    ChartJS.register(ArcElement, Tooltip, Legend)

    export default {
    name: 'App',
    components: {
        Doughnut
    },
    data() {
        return progressConfig
    }
    }
</script>

<style scoped>
    .wrapper {
        height: 50vh;
        margin-bottom: 40px;
    }
</style>