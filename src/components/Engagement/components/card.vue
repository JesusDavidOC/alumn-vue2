<template>
  <b-card>
    <b-card-body>
      <b-container>
        <b-row class="justify-content-md-center mt-5 mb-5">
          <b-col cols="auto">
            <img :src="getImgUrl()" alt="" height="90" />
          </b-col>
        </b-row>
        <b-row>
          <b-col class="col-card-title">
            <h5>
              <b>{{ card.title }}</b>
            </h5>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="col-card-body-text">
            <p>{{ card.bodyText }}</p>
          </b-col>
        </b-row>
      </b-container>
    </b-card-body>
  </b-card>
</template>

<script>
export default {
  name: "CardComponent",
  components: {},
  props: ["card"],
  methods: {
    getImgUrl() {
      return require("../assets/" + this.card.img + ".png");
    },
  },
};
</script>

<style scoped>
.col-card-title,
.col-card-body-text {
  text-align: center;
}

.col-card-body-text {
  color: rgba(0, 0, 0, 0.6);
}

.card {
  height: 100%;
}
</style>
