<template>
  <div class="bar-chart">
    <div v-for="(item, index) in computedValue" :key="index" class="bar" v-bind:style="item.style">{{ item.item }}</div>
  </div>
</template>

<script>
export default {
  name: 'BarChart',
  props: {
    value: Array,
  },
  computed: {
    computedValue() {
      const max = Math.max(...this.value);

      return this.value.map((item) => {
        return {
          item,
          style: {
            width: `${100 / this.value.length - 2}%`,
            height: `${(item * 100) / max}%`,
          },
        };
      });
    },
  },
};
</script>

<style>
.bar {
  background: red;
}
.bar-chart {
  width: 400px;
  height: 200px;
  display: flex;
  align-items: flex-end;
  justify-content: space-around;
}
</style>
