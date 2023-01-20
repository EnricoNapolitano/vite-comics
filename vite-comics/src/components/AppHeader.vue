<script>
import MainNav from './smaller_components/MainNav.vue'
export default {
    name: 'AppHeader',
    components: { MainNav }
}
</script>

<template>
    <header class="container">
        <!-- main navabar in header -->
        <nav>
            <figure><img src="../assets/img/dc-logo.png" alt="logo DC"></figure>
            <main-nav></main-nav>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partial/mixins.scss' as *;

nav {
    height: 120px;
    @include flex-jsb-ac; //display flex, justify content space between, align-itmes center
}

figure {
    width: 85px;
    height: 85px;
}
</style>