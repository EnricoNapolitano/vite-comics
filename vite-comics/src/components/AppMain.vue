<script>
import ComicCard from './smaller_components/ComicCard.vue';
export default {
    props: { comics: Array },
    components: { ComicCard }
}
</script>

<template>

    <main>
        <ul class="container flex-jc-ac wrap">
            <!-- component "ComicCard". Inside the string also the "comic" attribute to prepare the prop to pass -->
            <comic-card v-for="comic in comics" :key="comic.series" :comic="comic"></comic-card>
        </ul>
        <div class="container flex-jc-ac">
            <button>load more</button>
        </div>
    </main>
</template>

<style lang="scss">
@use '../assets/scss/partial/mixins.scss' as *;
@use '../assets/scss/partial/variables.scss' as *;

main {
    min-height: 130px;
    background-color: $black; //color from variablse.scss
    color: white;

    ul {
        padding: 40px 0;

        li {
            flex-basis: calc(100% / 6);
        }
    }

    button {
        @include button;
    }
}
</style>