<script>
export default {
    name: 'ProductCard',
    props: {
        brand: String,
        model: String,
        price: Number,
        badges: Array,
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
            <div class="fav flex">
                <button :class="{ 'true': favorite, 'false': !favorite }" @click="favorite = !favorite"><i
                        class="fa-solid fa-heart"></i></button>
            </div>

            <div class="boxes flex">
                <div class="box red" v-if="badges[badges.length - 1].type == 'discount'">{{ badges[badges.length -
                    1].value }}
                </div>
                <div class="box green" v-if="badges[0].type == 'tag'">Sostenibilità</div>
            </div>

            <img :src="'/img/' + imageFirst" alt="" class="first-img">
            <img :src="'/img/' + imageSecond" alt="">
        </div>
        <div class="card-text">
            <p class="brand">{{ brand }}</p>
            <h2>{{ model }}</h2>
            <p class="final-price" v-if="badges[badges.length - 1].type == 'discount'">
                {{ (price + (price * parseFloat(badges[badges.length - 1].value) / 100)).toFixed(0) - 0.01 }} €
            </p>
            <p class="final-price" v-else>{{ price }} €</p>
            <span class="old-price" v-if="badges[badges.length - 1].type == 'discount'">{{ price }} €
            </span>
        </div>
    </div>

</template>

<style lang="scss"></style>