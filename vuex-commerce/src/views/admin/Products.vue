<template>
  <div>
    <router-link to="/admin/product-add">Add new book</router-link>
    <ProductList />
  </div>
</template>

<script>
import ProductList from "@/components/admin/ProductList";

export default {
  components: {
    ProductList,
  },
  name: "Products"
}
</script>

<style scoped>

</style>