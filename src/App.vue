<template>
  <div id="app">
    <Header />
    <Products />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Products from './components/Products.vue';

export default {
  name: 'App',
  components: {
    Header,
    Products
  }
}
</script>

<style>
body {
  font-family: Arial, sans-serif;
}
</style>
