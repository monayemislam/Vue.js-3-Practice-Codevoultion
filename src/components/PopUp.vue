<template>
  <div>
    <h2>Pop up message</h2>
    <input type="text" v-model="name">
    <button @click="$emit('close',name)">Hide</button>
  </div>
</template>

<script>
export default {
    name: 'PopUp',
    emits: {
      close: (name)=>{
        if(!name){
          return false;
        }
        else{
          return true;
        }
      }
    },
    data(){
      return{
        name: ''
      }
    }
}
</script>

<style>

</style>