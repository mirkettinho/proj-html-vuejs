
<script>
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"
import SliderReviews from "./components/SliderReviews.vue"
import Main from "./components/Main.vue"


export default {
  name: "App",
  components: {
    Header,
    Footer,
    SliderReviews,
    Main
  }
}
</script>

<template>

<!-- HEADER -->
  <Header />

<!-- SLIDER REVIEWS -->
  <SliderReviews />

  <Main />
<!-- FOOTER -->
  <Footer />


</template>

<!-- SCSS -->
<style lang="scss">

// STILI GENERALI
@use "./scss/main.scss";

</style>