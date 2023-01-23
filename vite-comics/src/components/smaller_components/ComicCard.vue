<script>
export default {
    name: 'ComicCard',
    props: {
        comic: Object //imported single comic element from AppMain
    }
}
</script>

<template>
    <!-- Single comic: this is the component that will be repeated -->
    <li>
        <div>
            <figure>
                <a href="#"><img :src="comic.thumb" :alt="comic.series"></a>
            </figure>
            <h5>{{ comic.series }}</h5>
        </div>
    </li>
</template>

<style lang="scss" scoped>
// specifi style to create the 'comic card'
figure {
    width: 185px;
    height: 185px;
    overflow: hidden;
}

h5 {
    text-transform: uppercase;
    font-weight: 500;
    width: 90%;
    padding: 20px 0 30px 0;
}
</style>