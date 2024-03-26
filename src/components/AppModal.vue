<script>
export default {
    name: 'AppModal',
    props: {
        productId: Object
    }
}
</script>

<template>

    <div class="background" v-if="productId">
        <div class="modal">
            <h3>{{ productId.name }}</h3>
            <h5>{{ productId.brand }}</h5>
            <button @click="productId = null">x</button>
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
    text-align: center;
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

button {
    border: none;
    background-color: white;
    cursor: pointer;
}
</style>