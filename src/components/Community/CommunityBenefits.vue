<template>
  <b-container class="mt-5 pb-5" fluid>
    <b-row class="justify-content-md-center">
      <b-col cols="5">
        <b-row class="justify-content-md-center mt-5">
          <b-col cols="10">
            <h2 if="left-title">
              <b>Stay Connected With Your Community</b>
            </h2>
          </b-col>
        </b-row>
        <b-row v-for="card in cards" cols="4" :key="'community' + card.img">
          <b-col cols="12"> <CardComponent :card="card" /></b-col>
        </b-row>
      </b-col>
      <b-col cols="6">
        <img :src="getImgUrl()" alt="" class="h-100">
      </b-col>
    </b-row>
    <b-row> </b-row>
  </b-container>
</template>

<script>
import CardComponent from "./components/card.vue";
export default {
  name: "EngagementComponent",
  components: {
    CardComponent,
  },
  data() {
    return {
      cards: [
        {
          img: "first",
          title: "Content creation & sharing",
          bodyText:
            "Stay connected with your people by using our live chat and messaging applications.",
        },
        {
          img: "second",
          title: "Creation of events & tasks",
          bodyText:
            "Build constructive feedback posts and threads to encourage the engagement of your students and clients.",
        },
        {
          img: "third",
          title: "Calendar sharing",
          bodyText:
            "Become more productive and stay engaged  through our easy to use, minimalistic and memorizing interfaces.",
        },
      ],
    };
  },
  methods:{
    getImgUrl() {
      return require("./assets/bg-left.png");
    },
  }
};
</script>

<style scoped>
#left-title{
  text-align: start;
}
</style>
