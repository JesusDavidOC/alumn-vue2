<template>
  <b-container id="header" fluid>
    <b-row>
      <b-navbar toggleable="lg">
        <b-navbar-brand href="#" id="navbar-component"
          ><img alt="logo iris" src="../../assets/logo-iris.png" height="73px"
        /></b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-container class="text-light text-center"
          ><b-row class="w-100 justify-content-md-end">
            <b-col cols="2" class="headers-buttons-fonts"
              ><a href="">Why Iris?</a></b-col
            >
            <b-col cols="2" class="headers-buttons-fonts"
              ><a href=""> Benefits </a></b-col
            >
            <b-col cols="2" class="headers-buttons-fonts"
              ><a href=""> Testimonies </a></b-col
            >
            <b-col cols="2">
              <GetInTouchComponent />
            </b-col> </b-row
        ></b-container>
      </b-navbar>
    </b-row>
    <b-row align-h="end" class="mt-8">
      <b-col cols="4">
        <p id="header-text">
          The Learning Management Platform For All Teaching and Coaching
          Environments
        </p>
      </b-col>
      <b-col cols="2"></b-col>
    </b-row>
    <b-row align-h="end" class="mt-2">
      <b-col cols="3">
        <h1 class="title">Iris Co-Learning</h1>
      </b-col>
    </b-row>
    <b-row> </b-row>
  </b-container>
</template>

<script>
import GetInTouchComponent from "../shared/GetInTouch.vue";
export default {
  name: "HeaderComponent",
  components: {
    GetInTouchComponent,
  },
};
</script>

<style scoped>
#header {
  height: 800px;
  background-image: url("../../assets/backgroud-header.png");
  background-repeat: no-repeat;
  background-size: cover;
}

#navbar-component {
  margin: 1em 3em 2em;
}

.items-container {
  float: right;
}

.headers-buttons-fonts {
  text-align: center;
  a {
    text-decoration: none;
    color: white !important;
    font-size: 1.2em !important;
    font-weight: 600 !important;
  }
}

#button-header-nav {
  background-color: #ee983c;
  border-color: #ee983c;
  color: white !important;
  font-size: 1.1em !important;
  font-weight: 500 !important;
}

#header-text {
  color: white !important;
  font-size: 2em !important;
  font-weight: 500 !important;
  text-align: start;
}
</style>
