<template>
  <div style="margin: 8px 0">
    {{ product.name }}
  </div>
</template>

<script>
export default {
  name: "ProductItem",
  props: {
    product: Object
  }
};
</script>
