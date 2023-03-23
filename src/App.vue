<template>
<button @click="showPopUp=true">Show</button>
  <PopUp v-show="showPopUp" @close="showPopUpMethod"/>
</template>

<script>
import PopUp from './components/PopUp.vue';
export default {
  name: "App",
  components: {
    PopUp
  },
  data() {
    return {
      showPopUp: false
    };
  },
  methods: {
    showPopUpMethod(name){
      this.showPopUp=false,
      console.log('name: ',name)
    }
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
