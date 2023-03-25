<template>
  <div class="card">
        <slot>Default Content</slot>
  </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Card'
}
</script>

<style>
.card{
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    padding: 16px;
    transition: 0.3s;
    margin-bottom: 20px;
    width: 200px;
}
</style>