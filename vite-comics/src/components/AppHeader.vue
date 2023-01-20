<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            // data structure of navbar in header
            nav: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]

        }
    }
}
</script>

<template>
    <header class="container">
        <!-- main navabar in header -->
        <nav>
            <figure><img src="../assets/img/dc-logo.png" alt="logo DC"></figure>
            <ul>
                <li v-for="el in nav" :key="el.text"><a href="#">{{ el.text }}</a></li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partial/mixins.scss' as *;

nav {
    height: 120px;
    @include flex-jsb-ac; //display flex, justify content space between, align-itmes center
}

ul {
    @include flex-jsb; //display flex, justify content space between
}

li {
    text-transform: uppercase;
}

a {
    padding: 15px;
}
</style>