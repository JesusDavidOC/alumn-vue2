<template>
  <div id="alumn">
    <HeaderComponent />
    <IntroComponent />
    <EngagementComponent />
    <CommunityComponent />
    <Form />
    <Footer />
  </div>
</template>

<script>
import HeaderComponent from "./components/Header/Header.vue";
import IntroComponent from "./components/Intro/Intro.vue";
import EngagementComponent from "./components/Engagement/EngagementBenefits.vue";
import CommunityComponent from "./components/Community/CommunityBenefits.vue";
import Form from "./components/Form/Form.vue";
import Footer from "./components/Footer/Footer.vue";
export default {
  name: "App",
  components: {
    HeaderComponent,
    IntroComponent,
    EngagementComponent,
    CommunityComponent,
    Form,
    Footer,
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Montserrat" !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.title {
  color: white;
  font-weight: 600;
}
.mt-8 {
  margin-top: 6rem !important;
}
.pr-5 {
  padding-right: 3rem;
}
.pl-5 {
  padding-left: 3rem;
}
.ml-2{
  margin-left: 1.5rem;
}
.no-border {
  border: none !important;
}
a,p,b,span,h1,h2,h3,h4,h5,h6, button{ /*srry y didn't have so much time for integrate the fonts globaly*/
  font-family: "Montserrat" !important;
  font-size: 90%;
}
</style>
