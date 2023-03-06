<template>
<div>{{greet}} {{ name }}</div>
<div v-html="channel"></div>
<div v-html="hack"></div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      greet: "Hello",
      name: "Monayem",
      channel: "<b>Return One</b>",
      hack: `<a href="#" onClick="alert('You have been hacked!')">Win a Prize</a>`
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
