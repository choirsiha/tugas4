<!-- ChildComponent.vue -->
<template>
  <div class="child-component">
    <h2>Child Component</h2>
    <button @click="emitData">Send Data to Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitData() {
      this.$emit('dataEmitted', 'Hello from Child');
    }
  }
};
</script>

<style scoped>
.child-component {
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.child-component h2 {
  margin-top: 0;
}

.child-component button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.child-component button:hover {
  background-color: #0056b3;
}
</style>
