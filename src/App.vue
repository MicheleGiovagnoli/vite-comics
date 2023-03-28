<script >
import TheHeader from './components/TheHeader.vue';
import TheBlueBanner from './components/TheBlueBanner.vue';
import TheFooter from './components/TheFooter.vue';
import TheMain from './components/TheMain.vue';

export default {
  components: {
    TheHeader,
    TheBlueBanner,
    TheFooter,
    TheMain,
  },
  data() {
    return {
      cards: [
        {
          "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
          "price": "$19.99",
          "series": "Bloom",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
          "price": "$3.99",
          "series": "Black Adam",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
          "price": "$16.99",
          "series": "Swampthing",
          "type": "graphic novel"
        },
        {
          "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
          "price": "$2.99",
          "series": "Milestone",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
          "price": "$3.99",
          "series": "Milestone2",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
          "price": "$2.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
          "price": "$3.99",
          "series": "NightWing",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
          "price": "$4.99",
          "series": "Flash",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
          "price": "$5.99",
          "series": "Dc Connect",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
          "price": "$6.99",
          "series": "Robin",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
          "price": "$4.99",
          "series": "Lazarus",
          "type": "comic book"
        },
        {
          "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
          "price": "$16.99",
          "series": "Superman",
          "type": "graphic novel"
        }
      ]
    };
  },
  methods: {},
};
</script>

<template>
  <!-- HEADER -->
  <TheHeader />

  <!-- MAIN -->
  <main>
    <TheMain :passaggio="cards" />
  </main>

  <!-- BANNER -->
  <TheBlueBanner />

  <!-- FOOTER -->
  <TheFooter />
</template>

<style></style>
