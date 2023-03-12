<template>
  <div>
    <h2 v-once>{{ name }}</h2>
  </div>
  <div>
    <button @click="name = 'Batman'">Change Name</button>
  </div>
  <h2 v-pre>{{ name }}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Monayem",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
label {
  font-weight: bold;
  display: flex;
  margin-right: 20px;
  margin-top: 10px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.43;
  color: #555;
  background-color: #fff;
  margin-top: 5px;
  background-image: none;
}
</style>
