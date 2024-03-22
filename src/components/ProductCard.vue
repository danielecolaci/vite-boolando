<script>
export default {
    name: 'ProductCard',
    props: {
        brand: String,
        model: String,
        finalPrice: String,
        oldPrice: String,
        discountPercentage: Number,
        sustainability: Boolean,
        imageFirst: String,
        imageSecond: String,
        product: Object
    },
    data() {
        return {

        }
    }
}
</script>

<template>

    <div class="card">
        <div class="card-img">
            <div class="fav">
                <button><i class="fa-solid fa-heart"></i></button>
            </div>

            <div class="boxes flex">
                <div class="box red">-50%</div>
                <div class="box green">Sostenibilità</div>
            </div>

            <img :src="imageFirst" alt="" class="first-img">
            <img :src="imageSecond" alt="">
        </div>
        <div class="card-text">
            <p class="brand">{{ brand }}</p>
            <h2>{{ model }}</h2>
            <p class="final-price">{{ finalPrice }}</p>
            <span class="old-price">{{ oldPrice }}</span>
        </div>
    </div>

</template>

<style lang="scss"></style>