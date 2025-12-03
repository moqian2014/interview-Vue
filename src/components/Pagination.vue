<template>
  <div style="margin-top: 16px">
    <button 
      :disabled="page <= 1"
      @click="$emit('change', page - 1)"
    >
      Prev
    </button>

    <span style="margin: 0 8px">{{ page }}</span>

    <button 
      :disabled="page >= Math.ceil(total / pageSize)"
      @click="$emit('change', page + 1)"
    >
      Next
    </button>
  </div>
</template>

<script>
export default {
  name: "Pagination",
  props: {
    page: Number,
    pageSize: Number,
    total: Number
  }
};
</script>
