<!-- ParentComponent.vue -->
<template>
  <div class="parent-container">
    <h1>Nested Component Example</h1>
    <div class="nested-components">
      <ChildComponent @dataEmitted="handleData"></ChildComponent>
      <SlotComponent>
        <p>This content will be displayed in the slot of SlotComponent.</p>
      </SlotComponent>
    </div>
    <p>Data from Child: {{ childData }}</p>
    <button @click="resetData">Reset Data</button>
  </div>
</template>

<script>
import ChildComponent from './components/ChildComponent.vue';
import SlotComponent from './components/SlotComponent.vue';

export default {
  components: {
    ChildComponent,
    SlotComponent
  },
  data() {
    return {
      childData: ''
    };
  },
  methods: {
    handleData(data) {
      this.childData = data;
    },
    resetData() {
      this.childData = '';
    }
  }
};
</script>

<style scoped>
.parent-container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #f9f9f9;
}

.nested-components {
  display: flex;
  justify-content: space-between;
}

.parent-container p {
  margin-top: 20px;
}

.parent-container button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.parent-container button:hover {
  background-color: #0056b3;
}
</style>
