<template>
  <div>
    <h2>Pop up message</h2>
    <button @click="$emit('close','MOnayem')">Hide</button>
  </div>
</template>

<script>
export default {
    name: 'PopUp',
    emits: ['close']
}
</script>

<style>

</style>