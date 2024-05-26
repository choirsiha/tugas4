<!-- SlotComponent.vue -->
<template>
  <div class="slot-component">
    <h2>Slot Component</h2>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'SlotComponent'
};
</script>

<style scoped>
.slot-component {
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.slot-component h2 {
  margin-top: 0;
}
</style>
