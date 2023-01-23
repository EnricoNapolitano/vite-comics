<script>
export default {
    name: 'BlueNav',
    data() {
        return {
            //navbar data structure
            nav: [
                {
                    text: 'Digital Comics',
                    img: 'buy-comics-digital-comics.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Merchandise',
                    img: 'buy-comics-merchandise.png',
                    url: '#',
                    current: true,
                },
                {
                    text: 'subscription',
                    img: 'buy-comics-subscriptions.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comic shop locator',
                    img: 'buy-comics-shop-locator.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC power visa',
                    img: 'buy-dc-power-visa.svg',
                    url: '#',
                    current: false,
                },
            ],
        }
    },
    methods: {
        //method to create path image
        buildImagePath(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        }
    }
}
</script>
<template>
    <div class="blue-nav flex-jsb-ac">
        <ul class="container flex-jsb-ac">
            <li v-for="el in nav" :key="el.text">
                <a class="flex-jsb-ac" :href="el.url">
                    <figure>
                        <img :src="buildImagePath(el.img)" :alt="icona">
                    </figure>
                    {{ el.text }}
                </a>
            </li>
        </ul>
    </div>
</template>
<style lang="scss">
@use '../assets/scss/partial/mixins.scss' as *;
@use '../assets/scss/partial/variables.scss' as *;

.blue-nav {
    background-color: $blue;
    height: 155px;

    img {
        width: 50px;
        padding-right: 10px;
    }

    li:nth-child(4) img {
        width: 40px;
    }

    ul {
        padding: 0;
    }

    li {
        padding: 10px;
        text-transform: uppercase;
    }

    a {
        padding: 15px;
        color: white;
    }
}
</style>