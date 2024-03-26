<script>
export default {
    name: 'AppModal'
}
</script>

<template>
    <div class="background">
        <div class="modal">
            <h2>model</h2>
            <h5>brand</h5>
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
</style>