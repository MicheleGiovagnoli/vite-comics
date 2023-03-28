<script>
export default {
    name: "TheMain",
    data() {
        return {}
    },
    props: {
        passaggio: Array
    }
}
</script>

<template>
    <div class="wrapper-main">
        <div class="team-titans">

        </div>

        <div v-for="(element, i) in passaggio" :key="i" class="cards">
            <img :src="element.thumb" :alt="element.type">
            <h3>
                {{ element.series }}
            </h3>
        </div>
    </div>
</template>

<style scope lang="scss">
.wrapper-main {
    background-color: black;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    .cards {
        width: calc(100% / 5);
        padding: 20px;
        color: white;
        font-size: 10px;
        text-transform: uppercase;


        img {
            width: 100%;
        }
    }

}
</style>