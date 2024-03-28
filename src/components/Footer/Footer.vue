<template>
  <b-container class="mt-5 mb-5">
    <b-row class="justify-content-md-between">
      <b-col cols="6">
        <b-container>
          <b-row>
            <b-col>
              <img :src="getImgUrl()" alt="" />
            </b-col>
          </b-row>
          <b-row>
            <b-col cols="10" class="ml-2 mt-4" id="text-footer-container">
              <h5>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. At
                nullam elit enim eget at vitae pellentesque malesuada et.
                Fringilla ligula id velit vitae.
              </h5>
            </b-col>
          </b-row>
        </b-container>
      </b-col>
      <b-col cols="4">
        <b-container>
          <b-row class="justify-content-md-between mt-3">
            <b-col cols="4">
              <h3><b>Contact</b></h3>
            </b-col>
            <b-col cols="5">
              <h3><b>Why Iris?</b></h3>
            </b-col>

            <b-col cols="4" class="mt-5 transparent-text">
              <p>Get in touch</p>
            </b-col>
          </b-row>
        </b-container>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "FooterComponent",
  components: {},
  methods: {
    getImgUrl() {
      return require("./assets/logo-footer.png");
    },
  },
};
</script>

<style scoped>
#text-footer-container {
  h5,
  .transparent-text p{
    color: rgba(0, 0, 0, 0.6);
  }
}
</style>
