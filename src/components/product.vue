<template>
    <div class="product-container">
        {{ counter }}        
        <section class="product">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p>Tag %%a</p>
                <div class="wish-button">
                    <p v-on:click="counter += 1">Add to Wishlist</p>
                    <a href=""><i class="fas fa-heart"></i></a>
                </div>
            </div>
            <p></p>
            <p></p>
        </section>
        <section class="product">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p>Tag %%a</p>
                <div class="wish-button">
                    <p>Add to Wishlist</p>
                    <a href=""><i class="fas fa-heart"></i></a>
                </div>
            </div>
            <p></p>
            <p></p>
        </section>
        <section class="product">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p>Tag %%a</p>
                <div class="wish-button">
                    <p>Add to Wishlist</p>
                    <a href=""><i class="fas fa-heart"></i></a>
                </div>
            </div>
            <p></p>
            <p></p>
        </section>
        <section class="product">
            <div class="image-container">
                <img src="../assets/images/Group.png" alt="Product Image">
                <p>Tag %%a</p>
                <div class="wish-button">
                    <p>Add to Wishlist</p>
                    <a href=""><i class="fas fa-heart"></i></a>
                </div>
            </div>
            <p></p>
            <p></p>
        </section>
        
    </div>
</template>
<script>
export default {
  data: () => ({
    counter: 1
  })
};
</script>
