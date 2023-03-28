<script>
export default {
    name: "TheBlueBanner",
    data() {
        return {
            dcComics: ["Characters", "Comics", "Movies", "Tv", "Games", "Videos", "News"],
            dc: ["Terms Of Use", "Privacy Policy(New)", "Ad Choises", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
            sites: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],
            shop: ["Shop DC", "Shop DC Collectibles"],
            socials: [
                {
                    url: "footer-facebook.png",
                    name: "Facebook icon",
                },
                {
                    url: "footer-twitter.png",
                    name: "Twitter icon",
                },
                {
                    url: "footer-youtube.png",
                    name: "Youtube icon",
                },
                {
                    url: "footer-pinterest.png",
                    name: "Pinterest icon",
                },
                {
                    url: "footer-periscope.png",
                    name: "Periscope icon",
                },
            ],

        };
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="footer-top">
        <div class="wrapper">
            <div class="all">
                <div class="dc-container">
                    <h1>DC COMICS</h1>
                    <span v-for="(element, i) in dcComics" :key="i">{{ element }}</span>
                </div>
                <div class="dc-container">
                    <h1>DC</h1>
                    <span v-for="(element, i) in dc" :key="i">{{ element }}</span>
                </div>
                <div class="dc-container">
                    <h1>SITES</h1>
                    <span v-for="(element, i) in sites" :key="i">{{ element }}</span>
                </div>
                <div class="dc-container">
                    <h1>SHOP</h1>
                    <span v-for="(element, i) in shop" :key="i">{{ element }}</span>
                </div>
            </div>
            <div class="logo">

            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container">
            <div class="container-button">
                <span class="button">SIGN-UP NOW!</span>
            </div>
            <div class="social">
                <span>FOLLOW US</span>
                <img v-for="(social, i) in socials" :key="i" :src="getImagePath(social.url)" alt="social.name">
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins';



.footer-top {
    background: url(../assets/dc-logo-bg.png) right 20px no-repeat, url(../assets/footer-bg.jpg) top left repeat;

    .wrapper {
        width: 80%;
        display: flex;
        margin: auto;
        @include mixins.d-flex-space-between;

        .all {
            color: white;
            display: flex;
            flex-wrap: wrap;
            width: 50%;
            padding: 20px;


            .dc-container {
                padding: 10px;

                h1 {
                    font-size: 20px;
                }

                span {
                    color: grey;
                    display: block;

                    &:hover {
                        text-decoration: underline;
                        cursor: pointer;
                    }
                }
            }
        }

    }

    .logo {
        height: 100%;
        width: 50%;

        img {
            width: 100%;
        }
    }
}

.footer-bottom {
    background-color: rgb(48, 48, 48);
    position: relative;
    z-index: 2;
    height: 110px;
    display: flex;


    .container {
        width: 80%;
        margin: auto;
        @include mixins.d-flex-space-between;

        .container-button {
            .button {
                padding: 10px;
                color: white;
                border: solid 2px $color-primary;
                transition: all 0.5s ease;

                &:hover {
                    background-color: $color-primary;
                }
            }

        }

        .social {
            @include mixins.d-flex-space-between;

            span {
                color: $color-primary;
                padding: 10px;
                font-weight: bold;
            }

            img {
                padding: 10px;
                border-radius: 50%;
                transition: all 0.5s ease-in-out;

                &:hover {
                    background-color: $color-primary;
                }
            }


        }
    }
}
</style>