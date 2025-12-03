<template>
  <div>
    <h1>Vue 面试实操题 Demo</h1>

    <!-- 可手动切换不同题目 -->
    <!-- <TodoTest /> -->
    <!-- <CounterTest /> -->
    <!-- <ProductList /> -->

    <ProductList />
  </div>
</template>

<script>
import TodoTest from "./components/TodoTest.vue";
import CounterTest from "./components/CounterTest.vue";
import ProductList from "./components/ProductList.vue";

export default {
  components: { TodoTest, CounterTest, ProductList }
};
</script>
