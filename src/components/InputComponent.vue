<template>
  <input type="text"  :value="modelValue" @input="$emit('update:modelValue',$event.target.value)">
</template>

<script>
export default {
  name: 'InputComponent',
   props:{
    modelValue: String
  }
}
</script>

<style scooped>
input[type='text']{
    display: block;
    color: black;
    background-color: white;
    padding: 15px 30px;
}
</style>