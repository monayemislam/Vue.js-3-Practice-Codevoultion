<template>
  <div class="card">
    <div id="card-header">
        <slot name="card-header"></slot>
    </div>
    <div>
        <slot></slot>
    </div>
    <div id="card-footer">
        <slot name="card-footer"></slot>
    </div>
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