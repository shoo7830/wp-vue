<template>
  <div id="app">
    <post-list></post-list>
    <product-list></product-list>
  </div>
</template>

<script>
import PostList from './components/PostList';
import ProductList from './components/ProductList';

export default {
  components: {
    PostList,
    ProductList
  }
}
</script>

<style lang='css'>
@import 'http://static.gabia.com/gtris/1.2.0/css/gtris.css';
@import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.css';
</style>
