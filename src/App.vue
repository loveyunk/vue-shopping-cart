<template>
  <div id="app">
    <h1>Shoppint Cart Example</h1>
    <hr />
    <h2>Products</h2>
    <hr />
    <ProductList />
    <hr />
    <ShoppingCart />
  </div>
</template>

<script>
import ProductList from '@/components/ProductList/index.vue';
import ShoppingCart from '@/components/ShoppingCart/index.vue';

export default {
  name: 'app',
  components: {
    ProductList,
    ShoppingCart
  }
};
</script>
