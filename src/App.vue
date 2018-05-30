<template>
  <div id="app" class="container">
    <Header/>
    <ViewMode/>
    <Product/>
  </div>
</template>

<script>
import Header from './components/shared/header.vue'
import ViewMode from './components/viewMode.vue'
import Product from './components/product.vue'
export default {
  components: {
    Header,
    ViewMode,
    Product
  }
}
</script>

<style lang="scss">
@import 'assets/sass/app.scss'
</style>
