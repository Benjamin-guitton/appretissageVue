<template>
  <div>
    <h1>Cart</h1>
    <div v-if="cart">
      <div class="product" v-for="product in cart.products" :key="product.id">
        <i @click="incrementQuantity(product)"
           class="far fa-plus-square fa-lg">

        </i>
        <i @click="decrementQuantity(product)"
           class="far fa-minus-square fa-lg">

        </i>
        <span class="quantity">{{ product.quantity }}</span>
         {{ product.title }} - {{ product.price }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    incrementQuantity(product) {
        this.$store.dispatch("updateCart", product)
      },
      decrementQuantity(product) {
        this.$store.dispatch("removeOneFromCart", product)
      },
    },
  name: "Cart",
  computed: {
    cart() {
      return this.$store.getters.getCart;
    }
  },
};

</script>

<style scoped>
.quantity {
  border: 1px solid black;
  padding: 3px;
  margin: 3px;
  font-size: 17px;
  font-weight: bold;
}
.product {
  height: 89px;
  width: 80%;
  margin: 25px;
  border-bottom: 1px solid #ccc;
}

</style>