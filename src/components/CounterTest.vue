<template>
  <div>
    <h3>Count: {{ count }}</h3>
    <h4>Double: {{ doubleCount }}</h4>

    <button @click="count--">-</button>
    <button @click="count++">+</button>
  </div>
</template>

<script>
export default {
  name: "CounterTest",
  data() {
    return {
      count: 0
    };
  },
  computed: {
    doubleCount() {
      // 面试者补全
      return this.count * 2;
    }
  },
  watch: {
    count(newVal) {
      // 面试者补全
      if (newVal > 10) {
        alert("Too big");
      }
    }
  }
};
</script>
