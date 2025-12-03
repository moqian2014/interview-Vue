<template>
  <div class="p-4">
    <h2>Todo List</h2>
    <input v-model="newItem" placeholder="Add something..." />
    <button @click="addItem">Add</button>

    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
        <button @click="removeItem(index)">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TodoTest",
  data() {
    return {
      newItem: "",
      items: ["Buy milk", "Learn Vue"]
    };
  },
  methods: {
    addItem() {
      // 面试者需要补全
      if (!this.newItem.trim()) return;
      this.items.push(this.newItem.trim());
      this.newItem = "";
    },
    removeItem(index) {
      // 面试者需要补全
      this.items.splice(index, 1);
    }
  }
};
</script>
