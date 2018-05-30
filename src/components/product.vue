<template>
    <div class="product-container">
        <section class="product" id="produtos">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p class="tag">Tag %%</p>
                <div class="wish-button" id="wish" @click='sendWish()'>
                    <p class="wishlist">Add to Wishlist</p>
                    <a><i class="far fa-heart"></i></a>
                </div>
            </div>
            <div class="product-info">
                <p>Product name in a catalog page.Lorem ipsum dolor sit amet, consectetur...</p>
                <div class="price">
                    <p><span>R$0000,00</span> á vista</p>
                    <p>00x <span>R$ 00,00 s/juros</span></p>
                </div>
            </div>
        </section>
        <section class="product" id="produtos">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p class="tag">Tag %%</p>
                <div class="wish-button" id="wish" @click='sendWish()'>
                    <p class="wishlist">Add to Wishlist</p>
                    <a><i class="far fa-heart"></i></a>
                </div>
            </div>
            <div class="product-info">
                <p>Product name in a catalog page.Lorem ipsum dolor sit amet, consectetur...</p>
                <div class="price">
                    <p><span>R$0000,00</span> á vista</p>
                    <p>00x <span>R$ 00,00 s/juros</span></p>
                </div>
            </div>
        </section>
        <section class="product" id="produtos">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p class="tag">Tag %%</p>
                <div class="wish-button" id="wish" @click='sendWish()'>
                    <p class="wishlist">Add to Wishlist</p>
                    <a><i class="far fa-heart"></i></a>
                </div>
            </div>
            <div class="product-info">
                <p>Product name in a catalog page.Lorem ipsum dolor sit amet, consectetur...</p>
                <div class="price">
                    <p><span>R$0000,00</span> á vista</p>
                    <p>00x <span>R$ 00,00 s/juros</span></p>
                </div>
            </div>
        </section>
        <section class="product" id="produtos">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p class="tag">Tag %%</p>
                <div class="wish-button" id="wish" @click='sendWish()'>
                    <p class="wishlist">Add to Wishlist</p>
                    <a><i class="far fa-heart"></i></a>
                </div>
            </div>
            <div class="product-info">
                <p>Product name in a catalog page.Lorem ipsum dolor sit amet, consectetur...</p>
                <div class="price">
                    <p><span>R$0000,00</span> á vista</p>
                    <p>00x <span>R$ 00,00 s/juros</span></p>
                </div>
            </div>
        </section>
    </div>
</template>
<script>
import eventbus from '../utils/events/eventbus'
export default {
  data () {
    return {
      wish: 0
    }
  },
  created () {
    eventbus.$on('clickbutton', 
    function(param) {
        if(param === 'grid') {
            var el = document.querySelectorAll('.product');
            for(var i = 0; i < el.length; i++){
                el[i].classList.add('product-grid')
                el[i].classList.remove('product-list')
            }
        }
        if(param === 'block') {
            var el = document.querySelectorAll('.product');
            for(var i = 0; i < el.length; i++){
                el[i].classList.remove('product-grid')
                el[i].classList.remove('product-list')
            }
        }
        if(param === 'list') {
            var el = document.querySelectorAll('.product');
            for(var i = 0; i < el.length; i++){
                el[i].classList.remove('product-grid')
                el[i].classList.add('product-list')
            }
        }
        return param
    })
  },
  methods: {
    sendWish () {
    var ele = document.querySelectorAll('.wish-button');
    ele.forEach((el) => {
    el.addEventListener('click', () => {
        el.classList.add('add-wish');
        });
    });
    var increment = ++this.wish
    eventbus.$emit('sendwish', increment)
    }
  }
}
</script>
