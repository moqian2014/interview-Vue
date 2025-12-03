<template>
  <div class="p-4">
    <input v-model="keyword" placeholder="Search..." />

    <ProductItem 
      v-for="item in pagedList" 
      :key="item.id" 
      :product="item" 
    />

    <Pagination 
      :page="page" 
      :page-size="pageSize"
      :total="filteredList.length"
      @change="handlePageChange"
    />
  </div>
</template>

<script>
import ProductItem from "./ProductItem.vue";
import Pagination from "./Pagination.vue";

export default {
  name: "ProductList",
  components: { ProductItem, Pagination },
  data() {
    return {
      keyword: "",
      page: 1,
      pageSize: 3,
      list: [
        { id: 1, name: "Apple" },
        { id: 2, name: "Orange" },
        { id: 3, name: "Banana" },
        { id: 4, name: "Watermelon" },
        { id: 5, name: "Pear" }
      ]
    };
  },
  computed: {
    filteredList() {
      // 面试者补全
      return this.list.filter(item =>
        item.name.toLowerCase().includes(this.keyword.toLowerCase())
      );
    },
    pagedList() {
      // 面试者补全
      const start = (this.page - 1) * this.pageSize;
      return this.filteredList.slice(start, start + this.pageSize);
    }
  },
  methods: {
    handlePageChange(newPage) {
      // 面试者补全
      this.page = newPage;
    }
  }
};
</script>
