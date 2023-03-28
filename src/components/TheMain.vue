<script>
export default {
    name: "TheMain",
    data() {
        return {
            variabile: false,
        }
    },
    methods: {
        showSeries() {
            if (this.variabile == false) {
                this.variabile = true;
            } else if (this.variabile == true) {
                this.variabile = false;
            }
            console.log(this.variabile);
        }

    },
    props: {
        passaggio: Array
    },
}
</script>

<template>
    <div class="wrapper-main">
        <div class="team-titans">
            <div class="button-blue" @click="showSeries()">
                <h2>CURRENT SERIES</h2>
            </div>

        </div>

        <div class="cards-container" v-show="variabile == true">
            <div v-for="(element, i) in passaggio" :key="i" class="cards">
                <img :src="element.thumb" :alt="element.type">
                <h3>
                    {{ element.series }}
                </h3>
            </div>
            <div class="button-blue">
                <span>LOAD MORE</span>
            </div>
        </div>
    </div>
</template>

<style scope lang="scss">
@use "../styles/partials/variables" as*;
@use "../styles/partials/mixins";

.wrapper-main {
    background-color: rgb(28, 28, 28);

    .team-titans {
        height: 400px;
        background-image: url(../assets/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;

        .button-blue {
            color: white;
            font-weight: bold;
            position: absolute;
            bottom: -5%;
            left: 10%;
            cursor: pointer;
            transition: all 0.5s ease;

            &:hover {
                color: black;
                bottom: 0px;
            }

            h2 {
                background-color: $color-primary;
                padding: 10px;
                margin: 0px;
            }
        }
    }

    .cards-container {
        width: 80%;
        margin: auto;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        padding: 50px 0px;

        .cards {
            width: calc((100% / 6) - 20px);
            padding: 30px 20px;
            color: white;
            font-size: 10px;
            text-transform: uppercase;

            img {
                width: 100%;
                height: 100%;
            }
        }

        .button-blue {
            color: white;
            width: 100%;
            text-align: center;

            span {
                background-color: $color-primary;
                padding: 10px 30px;
            }
        }
    }
}
</style>