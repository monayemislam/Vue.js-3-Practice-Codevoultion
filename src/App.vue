<template>
  <h2>Full Name - {{ firstName }} {{ lastName }}</h2>
  <h2>Computed Full Name - {{ fullName }}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "Monayem",
      lastName: "Islam",
    };
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
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
