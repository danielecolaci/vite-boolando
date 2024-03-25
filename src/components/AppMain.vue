<script>
import ProductCard from './ProductCard.vue'
import { products } from '../data.js'
import { state } from '../state.js'

export default {
    name: 'AppMain',
    components: {
        ProductCard
    },
    data() {
        return {
            products,
            state
        }
    },
    mounted() {
        console.log(this.state);
        this.state.getProducts(this.state.product_api_url)
    }
}
</script>

<template>

    <main>
        <div class="flex main-container">

            <ProductCard v-for="product in products" :key="product.id" :brand="product.brand" :model="product.model"
                :finalPrice="product.finalPrice" :oldPrice="product.oldPrice"
                :discountPercentage="product.discountPercentage" :sustainability="product.sustainability"
                :imageFirst="product.imageFirst" :imageSecond="product.imageSecond" :favorite="product.favorite" />

        </div>
    </main>

</template>

<style lang="scss"></style>