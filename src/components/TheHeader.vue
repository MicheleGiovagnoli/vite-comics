<script>
export default {
    name: "TheHeader",
    data() {
        return {
            navLinks: [
                {
                    href: "#Characters",
                    text: "Characters"
                },
                {
                    href: "#Comics",
                    text: "Comics"
                },
                {
                    href: "#Movies",
                    text: "Movies"
                },
                {
                    href: "#Tv",
                    text: "Tv"
                },
                {
                    href: "#Games",
                    text: "Games"
                },
                {
                    href: "#Collectibles",
                    text: "Collectibles"
                },
                {
                    href: "#Video",
                    text: "Video"
                },
                {
                    href: "#Fans",
                    text: "Fans"
                },
                {
                    href: "#News",
                    text: "News"
                },
                {
                    href: "#Shop",
                    text: "Shop"
                },
            ],
        };
    },
};
</script>

<template>
    <header>
        <nav>
            <!-- Logo Brand -->
            <div class="brand">
                <img src="../assets/dc-logo.png" alt="Dc Logo">
            </div>

            <!-- Links -->
            <ul class="navbar">
                <li v-for="(link, i) in navLinks" :key="i">
                    <a class="link" href="link.href">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";

nav {
    display: flex;
    justify-content: space-between;
    width: 80%;
    height: 110px;
    margin: auto
}

.navbar {
    @include mixins.d-flex-center;
    list-style: none;

    //Annidamento
    .link {
        padding: 10px;
        padding-bottom: 40px;
        text-decoration: none;
        font-weight: bold;
        text-transform: uppercase;
        color: black;
        transition: color 0.3s ease;

        &:hover {
            color: $color-primary;
            border-bottom: solid 5px $color-primary;
        }
    }
}
</style>
