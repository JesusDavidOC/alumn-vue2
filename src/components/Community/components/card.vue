<template>
  <b-card class="img-left no-border pt-0 pm-0">
    <b-card-body class="pt-0 pm-0">
      <b-container>
        <b-row class="justify-content-md-between">
          <b-col cols="2">
            <img :src="getImgUrl()" alt="" height="90px"/>
          </b-col>
          <b-col cols="9">
            <b-row>
              <b-col class="col-card-title"
                ><h6>
                  <b>{{ card.title }}</b>
                </h6></b-col
              >
            </b-row>
            <b-row>
              <b-col class="col-card-body-text"
                ><p>{{ card.bodyText }}</p></b-col
              >
            </b-row>
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
  text-align: start;
}

.col-card-body-text {
  color: rgba(0, 0, 0, 0.6);
}

.card {
  height: 80%;
}
</style>
