<script >
import TheHeader from './components/TheHeader.vue';
import TheBlueBanner from './components/TheBlueBanner.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  components: {
    TheHeader,
    TheBlueBanner,
    TheFooter,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<template>
  <TheHeader />

  <main>
    <div class="container">
      <h2>Contents Go Here</h2>
    </div>
  </main>

  <TheBlueBanner />

  <TheFooter />
</template>

<style  lang="scss">
@use "./styles/general.scss";

main {
  background-color: black;
  height: 110px;
  display: flex;
  align-items: center;

  .container {
    width: 80%;
    margin: auto;

    h2 {
      color: white;
    }
  }
}
</style>
