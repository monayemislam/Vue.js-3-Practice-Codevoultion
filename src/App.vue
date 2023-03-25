<template>
<card></card>
<card>
  <h2>Hello</h2>
</card>
<card>
  <h2>Monayem Islam</h2>
</card>
<card>
  <img src="https://picsum.photos/200">
</card>
</template>

<script>
import Card from './components/Card.vue';
export default {
  name: "App",
  components: {
    Card
  },
  data() {
    return {
      name: '',
    };
  },
  methods: {
    
  }
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
