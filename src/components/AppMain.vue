<script>
import ProductCard from './ProductCard.vue'

export default {
    name: 'AppMain',
    components: {
        ProductCard
    },
    data() {
        return {

        }
    }
}
</script>

<template>

    <main>
        <div class="flex main-container">

            <ProductCard />

        </div>
    </main>

</template>

<style lang="scss"></style>