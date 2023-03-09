<template>
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Not A Number</h2>

  <div v-if="display">
    <h2>Monayem</h2>
    <h2>Return One</h2>
    <h2>Vue</h2>
  </div>

  <h2 v-show="showElement">Using v-show</h2>
  <h2 v-if="showElement">Using if</h2>
  <!-- Generally speaking, v-if has higher toggle costs while v-show has higher initial render costs. So prefer v-show if you need to toggle something very often, and prefer v-if if the condition is unlikely to change at runtime. -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      num: "Hi",
      display: true,
      showElement: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
