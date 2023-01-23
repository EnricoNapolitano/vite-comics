<script>
export default {
    name: 'DownerFooter',
    data() {
        return {
            //social icons list
            socials: [
                {
                    name: 'footer-facebook.png',
                    url: '#',
                },
                {
                    name: 'footer-twitter.png',
                    url: '#',
                },
                {
                    name: 'footer-youtube.png',
                    url: '#',
                },
                {
                    name: 'footer-pinterest.png',
                    url: '#',
                },
                {
                    name: 'footer-periscope.png',
                    url: '#',
                },
            ]
        }
    },
    methods: {
        //method to create path social icon
        buildIconPath(icon) {
            return new URL(`../../assets/img/${icon}`, import.meta.url).href;
        }
    }
}
</script>
<template>
    <footer class="downer-footer">
        <!-- Here starts the footer downside -->
        <div class="row flex-jsb-ac container">
            <button>SIGN-UP NOW!</button>
            <div class="flex flex-jsb-ac">
                <span>FOLLOW US</span>
                <!-- social icons -->
                <ul class="flex">
                    <li v-for="social in socials">
                        <a href="#"><img :src="buildIconPath(social.name)" alt="social icon"></a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
@use '../../assets/scss/partial/variables' as *;
@use '../../assets/scss/partial/mixins.scss' as *;

.downer-footer {
    background-color: $grey;

    button {
        padding: 15px 40px;
        border: 2px solid $blue;
        background-color: transparent;
        color: white;
        font-weight: bold;
        font-size: 12px;
        cursor: pointer;
    }

    span {
        font-family: "Open Sans Condensed", sans-serif;
        font-size: 20px;
        font-weight: bold;
        color: $blue;
    }

    div.row {
        height: 110px;
    }

    li {
        padding-left: 10px;
    }
}
</style>