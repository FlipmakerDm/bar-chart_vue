<template>
  <div id="app">
    <BarChart :value="value1" />
    <br />
    <BarChart :value="value2" />
  </div>
</template>

<script>
import BarChart from './components/BarChart.vue';
export default {
  name: 'App',
  components: { BarChart },
  data: () => ({
    value1: [23, 3, 45, 300, 10, 1, 64, 64],
    value2: [23, 3, 45, 10, 10, 1, 64, 88, 55, 89, 22, 44, 99],
  }),
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 1024px;
  margin: 60px auto;
}
</style>
