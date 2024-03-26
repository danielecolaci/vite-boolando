<script>
export default {
    name: 'AppModal',
    props: {
        productId: Object
    },
    methods: {
    }
}
</script>

<template>

    <div class="background" v-if="productId">
        <div class="modal flex">
            <div class="product-img flex">
                <img :src="'/img/' + productId.frontImage" alt="">
                <img :src="'/img/' + productId.backImage" alt="">
            </div>
            <div class="detail flex">
                <div class="card-text">
                    <p class="brand">{{ productId.brand }}</p>
                    <h3>{{ productId.name }}</h3>
                </div>
                <div class="price flex">
                    <span class="final-price">{{ productId.price }}</span>
                    <span class="old-price">{{ productId.price }}</span>
                </div>
                <button @click="productId = null">&Cross;</button>
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.modal {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    z-index: 100;
    flex-direction: column;
    gap: 10px;
    width: 60%;
    max-width: 800px;

    .product-img {
        width: 100%;
        justify-content: space-between;
        gap: 10px;

        img {
            width: 49%;
        }
    }

    .detail {
        justify-content: space-between;
        align-items: center;
    }

    .price {
        align-items: flex-end;
        gap: 10px;

        span {
            font-size: 20px;
        }
    }

    .old-price {
        text-decoration: line-through;
    }

    button {
        width: 40px;
        height: 40px;
        border: none;
        border-radius: 16px;
        background-color: white;
        cursor: pointer;
        position: absolute;
        top: 40px;
        right: 40px;
        font-size: 20px;
        font-weight: bolder;
    }
}

.background {
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    backdrop-filter: blur(1px);
    position: fixed;
    top: 0%;
    left: 0%;
    z-index: 90;
}
</style>