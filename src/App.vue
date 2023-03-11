<template>
   <h2>Add Number- {{add(4,5,6)}}</h2>
   <h2>Multiply Number- {{multiply(5)}}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
     baseNumber: 5
    }
  },
  methods: {
    add(a,b,c){
      return a+b+c;
    },
    multiply(num){
      return this.baseNumber*num;
    }
  }
}
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
