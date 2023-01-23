<script>
export default {
    name: 'CentralNav',
    props: { nav: Array },
    methods: {
        //method to create path image
        buildImagePath(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        }
    }
}
</script>
<template>
    <div class="central-nav flex-jsb-ac">
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
@use '../assets/scss/partial/variables.scss' as *;

.central-nav {
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