<script>
export default {
    name: "TheBlueBanner",
    data() {
        return {
            navOptions: [
                {
                    href: "#DigitalComics",
                    name: "Digital Comics",
                    img: "buy-comics-digital-comics.png",
                },
                {
                    href: "#DcMerchandise",
                    name: "Dc Merchandise",
                    img: "buy-comics-merchandise.png",
                },
                {
                    href: "#Subscription",
                    name: "Subscription",
                    img: "buy-comics-subscriptions.png",
                },
                {
                    href: "#ComicShopLocator",
                    name: "Comic Shop Locator",
                    img: "buy-comics-shop-locator.png",
                },
                {
                    href: "#DcPowerVisa",
                    name: "Dc Power Visa",
                    img: "buy-dc-power-visa.svg",
                },
            ],
        };
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/${img}`, import.meta.url).href;
        }

    }
};
</script>

<template>
    <div class="container">
        <ul>
            <li v-for="(options, i) in navOptions" :key="i">
                <a :href="options.href" class="card">
                    <img :src="getImagePath(options.img)" :alt="options.name">
                    <span>{{ options.name }}</span>
                </a>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as*;
@use "../styles/partials/mixins";

.container {
    background-color: $color-primary;
    height: 150px;
    @include mixins.d-flex-center;

    ul {
        @include mixins.d-flex-space-between;
        list-style: none;
        width: 80%;

        .card {
            padding: 10px;
            text-decoration: none;
            text-transform: uppercase;
            color: white;
            @include mixins.d-flex-center;

            span {
                font-size: 13px;
                padding: 10px;
            }

            img {
                width: 40px;
            }
        }

    }
}
</style>