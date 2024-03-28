<template>
  <b-container>
    <b-row class="mt-5" align-v="center">
      <b-col id="card-container">
        <b-card
          :img-src="getImgUrl()"
          img-alt="Card image"
          img-top
          class="no-border"
        >
          <b-card-text>
            <b>Iris Co-Learning</b> offers you a space where you can handle your
            daily coaching and teaching tasks, connect with your crowd and
            manage your time so you are free to enjoy the simple things of life.
          </b-card-text>
        </b-card>
      </b-col>
      <b-col id="intro-text-right">
        <b-container>
          <b-row class="justify-content-md-center">
            <b-col cols="10">
              <p id="first-text">
                Are you a <b>teacherpreneur, life coach</b> or a
                <b>mentor</b> who is struggling with connecting, engaging and
                managing your audience through boring, old fashioned and
                expensive digital learning management platforms?
              </p>
            </b-col>
          </b-row>
          <b-row class="justify-content-md-center mt-2">
            <b-col cols="10">
              <p id="second-text">
                Well don’t worry, we have heard your cries for help and we have
                you covered.
              </p>
            </b-col>
          </b-row>
          <b-row class="justify-content-md-center mt-2">
            <b-col cols="10">
              <b-row>
                <b-col>
                  <GetInTouchComponent />
                </b-col>
              </b-row>
            </b-col>
          </b-row>
        </b-container>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import GetInTouchComponent from "../shared/GetInTouch.vue";
export default {
  name: "IntroComponent",
  components: {
    GetInTouchComponent,
  },
  methods: {
    getImgUrl() {
      return require("../../assets/intro.png");
    },
  },
};
</script>

<style scoped>
#card-container {
  .card-text {
    color: rgba(0, 0, 0, 0.6);
  }
}

#intro-text-right {
  font-size: 1.2em;
  #second-text {
    font-weight: bolder;
    color: #c4007a;
  }
}
</style>
