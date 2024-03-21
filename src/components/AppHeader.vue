<script>
export default {
    name: 'AppHeader',
    data() {
        return {

        }
    }
}
</script>

<template>

    <header>
        <div class="flex header-container">
            <nav class="link">
                <ul>
                    <li><a href="">Donna</a></li>
                    <li><a href="">Uomo</a></li>
                    <li><a href="">Bambini</a></li>
                </ul>
            </nav>
            <div class="account-icon">
                <ul class="li-account">
                    <li><a href=""><i class="fa-regular fa-user"></i></a></li>
                    <li><a href=""><i class="fa-regular fa-heart"></i></a></li>
                    <li><a href=""><i class="fa-solid fa-bag-shopping"></i></a></li>
                </ul>
            </div>
        </div>
        <div class="logo">
            <img src="/img/boolando-logo.png" alt="">
        </div>
    </header>

</template>

<style lang="scss"></style>