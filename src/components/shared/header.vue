<template>
    <header class="header">
      <div class="menu">
        <nav class="menu-button">
            <a href=""><i class="fas fa-bars"></i></a>
        </nav>
        <img class="menu-img" src="../../assets/images/logo-lojaskd.png" alt="Logo Lojaskd">
        <div class="menu-icons">
            <a href="" class="wish-marker" :data-count='this.wish'><i class="fas fa-heart"></i></a>
            <a href=""><i class="fas fa-user"></i></a>
            <a href=""><i class="fas fa-shopping-cart"></i></a>
        </div>
      </div>
      <form action="" class="search-form">
        <input type="text" id="search" placeholder="Search field...">
        <button type="submit"><i class="fas fa-search"></i></button>
      </form>
      <div class="tag">
        <a>This is a tag</a>
        <a>This is a tag</a>
      </div>
    </header>
</template>
<script>
import eventbus from '../../utils/events/eventbus'
export default {
  data () {
    return {
      wish: 0
    }
  },
  created () {
    eventbus.$on('sendwish', 
    function(num) {
        this.wish = num
        return num
    }.bind(this))
  }
}
</script>
