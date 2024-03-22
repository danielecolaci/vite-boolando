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
        favorite: Boolean,
        product: Object
    }
}
</script>

<template>

    <div class="card">
        <div class="card-img">
            <div class="fav">
                <button :class="{ 'true': favorite, 'false': !favorite }" @click="favorite = !favorite"><i
                        class="fa-solid fa-heart"></i></button>
            </div>

            <div class="boxes flex">
                <div class="box red" v-if="discountPercentage !== null">-{{ discountPercentage }}%</div>
                <div class="box green" v-if="sustainability === true">Sostenibilità</div>
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