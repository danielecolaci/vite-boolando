<script>
import ProductCard from './ProductCard.vue'
import { state } from '../state.js'

export default {
    name: 'AppMain',
    components: {
        ProductCard
    },
    data() {
        return {
            state
        }
    },
    mounted() {
        /* console.log(this.state); */
        this.state.getProducts(this.state.product_api_url)
    }
}
</script>

<template>

    <main>
        <div class="flex main-container">

            <ProductCard v-for="product in state.products" :key="product.id" :brand="product.brand"
                :model="product.name" :price="product.price" :imageFirst="product.frontImage"
                :imageSecond="product.backImage" :favorite="product.isInFavorites" :badges="product.badges" />

        </div>
    </main>

</template>

<style lang="scss"></style>