<template>
  <div>
    <h3>Create a new book</h3>
    <ProductForm/>
  </div>

</template>

<script>
import ProductForm from "../../components/admin/ProductForm";

export default {
  components: {
    ProductForm
  },
  name: "ProductAdd"
}
</script>

<style scoped>

</style>