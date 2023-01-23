<script>
export default {
    name: 'MainNav',
    data() {
        return {
            // data structure of main navbar
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
            ],
        }
    }
}
</script>
<template>
    <ul class="flex-jsb-ac">
        <!-- class active if current is true -->
        <li :class="{ active: el.current }" class="flex-ac" v-for="el in nav" :key="el.text"><a :href="el.url">{{
            el.text
        }}</a>
        </li>
    </ul>
</template>
<style lang="scss" scoped>
@use '../../assets/scss/partial/mixins.scss' as *;
@use '../../assets/scss/partial/variables.scss' as *;

ul {
    height: 100%;
}

li {
    text-transform: uppercase;
    border: 5px solid transparent;
    height: 100%;

    &:hover {
        @include underline;
    }
}

li.active {
    @include underline;
}

a {
    font-family: "Open Sans Condensed", sans-serif;
    font-weight: bold;
    padding: 15px;
    color: $grey;

    &.active,
    &:hover {
        color: $blue;
    }
}
</style>