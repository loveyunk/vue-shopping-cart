<template>
  <ul>
    <li v-for="product in products" :key="product.id">
      {{ product.title }} - {{ product.price | currency }}
      <br />
      <button :disabled="!product.inventory" @click="addProductToCart(product)">
        Add to card
      </button>
    </li>
  </ul>
</template>

<script>
import { mapState, mapActions } from 'vuex';

export default {
  computed: {
    ...mapState({
      products: state => state.products.all
    })
  },
  created() {
    this.$store.dispatch('products/getAllProducts');
  },
  methods: {
    ...mapActions('cart', ['addProductToCart'])
  }
};
</script>
