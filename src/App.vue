<template>
  <div id="app">
    <!-- <post-list></post-list> -->
    <product-list></product-list>
  </div>
</template>

<script>
//import PostList from './components/PostList';
import ProductList from './components/ProductList';

export default {
  components: {
    // PostList
    ProductList
  }
}
</script>

<style lang='scss'>
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,textarea,p,blockquote,th,td,input,select,textarea,button {margin:0;padding:0}
fieldset,img {border:0 none}
dl,ul,ol,menu,li {list-style:none}
blockquote, q {quotes: none}
blockquote:before, blockquote:after,q:before, q:after {content:'';content:none}
input,select,textarea,button {vertical-align:middle}
input[type='text'],input[type='password']{-webkit-appearance:none;border-radius:0/*Safari/Chrome*/}
button {border:0 none;background-color:transparent;cursor:pointer}
body {background:#fff}
body,th,td,input,select,textarea,button {font-size:18px;line-height:1.5;font-family:Apple Gothic,"Malgun Gothic",dotum,"Arial", sans-serif;color:#333}
a {color:#333;text-decoration:none}
a:active, a:hover {text-decoration:none}
caption {visibility:hidden;overflow:hidden;width:1px;height:0;font-size:0;line-height:0;}
address,cite,code,dfn,em,var {font-style:normal;font-weight:normal}
table {border-collapse:collapse;border-spacing:0}
</style>
