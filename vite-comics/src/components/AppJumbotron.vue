<script>
export default {
    name: 'AppJumbotron',
    data() {
        return {
            jumbotron: 'jumbotron.jpg',
        }
    },
    methods: {
        //method to create jumbotron's path
        buildJumboPath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>
<template>
    <figure>
        <img :src="buildJumboPath(jumbotron)" alt="main banner picture">
    </figure>
</template>
<style lang="scss" scoped>
figure {
    height: 400px;
    overflow: hidden;
}

img {
    width: 100%;
}
</style>