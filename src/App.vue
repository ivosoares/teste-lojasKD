<template>
  <div id="app" class="container">
    <Header/>
    <ViewMode/>
  </div>
</template>

<script>
import Header from './components/shared/header.vue'
import ViewMode from './components/viewMode.vue'
export default {
  components: {
    Header,
    ViewMode
  }
}
</script>

<style lang="scss">
@import 'assets/sass/app.scss'
</style>
