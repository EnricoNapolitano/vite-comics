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
        <nav class="flex-jsb-ac">
            <figure><img src="../assets/img/dc-logo.png" alt="logo DC"></figure>
            <main-nav></main-nav>
        </nav>
    </header>
</template>

<style lang="scss">
@use '../assets/scss/partial/mixins.scss' as *;

header {
    nav {
        height: 120px;
    }

    figure {
        width: 85px;
        height: 85px;
    }
}
</style>