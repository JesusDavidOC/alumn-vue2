<template>
  <b-container id="engagement-container" class="mt-5 pb-5" fluid>
    <b-row class="justify-content-md-center">
      <b-col cols="9">
        <b-row class="justify-content-md-center mt-5">
          <b-col cols="auto">
            <h2 class="title"><b>Engage With Your Audience</b></h2>
          </b-col>
        </b-row>
        <b-row class="justify-content-md-center mt-2">
          <b-col id="subtitle-engagement" cols="auto">
            <p>
              <b>Iris</b> allows you to create engaging experiences through such
              features as:
            </p>
          </b-col>
        </b-row>
        <b-row class="justify-content-md-between mt-2">
          <b-col v-for="card in cards" cols="4" :key="card.img">
            <CardComponent :card="card"
          /></b-col>
        </b-row>
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
          title: "Live chat & Messaging",
          bodyText:
            "Stay connected with your people by using our live chat and messaging applications.",
        },
        {
          img: "second",
          title: "Feedback Threads",
          bodyText:
            "Build constructive feedback posts and threads to encourage the engagement of your students and clients.",
        },
        {
          img: "third",
          title: "User Experience",
          bodyText:
            "Become more productive and stay engaged  through our easy to use, minimalistic and memorizing interfaces.",
        },
      ],
    };
  },
};
</script>

<style scoped>
#engagement-container {
  background-color: #693188;
}
#subtitle-engagement {
  color: white;
}
</style>
