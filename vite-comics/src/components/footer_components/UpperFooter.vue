<script>
export default {
    data() {
        return {
            // data structure DC Comics in footer
            DcComicsList: [
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
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
            ],
            // data structure DC in footer
            DcList: [
                {
                    text: 'Terms of Use',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Ad choices',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Advertising',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Jobs',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Subscriptions',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Talent Workshops',
                    url: '#',
                    current: false,
                },
                {
                    text: 'CPSC Certificates',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Ratings',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop Help',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Contact Us',
                    url: '#',
                    current: false,
                },
            ],
            // data structure Site list in footer
            SitesList: [
                {
                    text: 'DC',
                    url: '#',
                    current: false,
                },
                {
                    text: 'MAD Magazine',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Kids',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Universe',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC Power Visa',
                    url: '#',
                    current: false,
                },
            ],
            // data structure Shop list in footer
            ShopList: [
                {
                    text: 'Shop DC',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}
</script>
<template>
    <footer class="upper-footer">
        <div class="row flex-jsb-ac container">
            <!-- groupping the footer lists -->
            <div class="flex">
                <div class="col">
                    <h3>DC Comics</h3>
                    <ul>
                        <li v-for="el in DcComicsList"><a href="#">{{ el.text }}</a></li>
                    </ul>
                    <div class="col">
                        <h3>Shop</h3>
                        <ul>
                            <li v-for="el in ShopList"><a href="#">{{ el.text }}</a></li>
                        </ul>
                    </div>
                </div>
                <div class="col">
                    <h3>DC</h3>
                    <ul>
                        <li v-for="el in DcList"><a href="#">{{ el.text }}</a></li>
                    </ul>
                </div>
                <div class="col">
                    <h3>Sites</h3>
                    <ul>
                        <li v-for="el in SitesList"><a href="#">{{ el.text }}</a></li>
                    </ul>
                </div>
            </div>
            <!-- DC big logo -->
            <figure class="flex-jc-ac">
                <img src="../../assets/img/dc-logo-bg.png" alt="logo DC">
            </figure>
        </div>
    </footer>
</template>
<style lang="scss">
@use '../../assets/scss/partial/mixins.scss' as *;
@use '../../assets/scss/partial/variables.scss' as *;

.upper-footer {
    height: calc(100vh - 515px);
    background-image: url('../../assets/img/footer-bg.jpg');
    background-size: cover;
    font-family: "Open Sans Condensed", sans-serif;

    figure {
        overflow: hidden;
        height: 100%;
    }

    .row {
        height: 100%;
    }

    h3 {
        text-transform: uppercase;
        padding: 20px 0;
        color: white;
    }

    ul {
        padding-right: 70px;
    }

    li {
        padding: 2px 0;
    }

    a {
        color: $light-grey;
        padding: 0;

        &:hover {
            color: $blue;
        }
    }
}
</style>