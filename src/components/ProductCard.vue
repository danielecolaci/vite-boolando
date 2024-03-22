<script>
export default {
    name: 'ProductCard',
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

            <img src="/img/1.webp" alt="" class="first-img">
            <img src="/img/1b.webp" alt="">
        </div>
        <div class="card-text">
            <p class="brand">Levi's</p>
            <h2>RELAXED FIT TEE UNISEX</h2>
            <p class="final-price">14,99 €</p>
            <span class="old-price">29,99 €</span>
        </div>
    </div>

</template>

<style lang="scss"></style>