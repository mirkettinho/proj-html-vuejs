
<script>
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"
import SliderReviews from "./components/SliderReviews.vue"


export default {
  name: "App",
  components: {
    Header,
    Footer,
    SliderReviews
  }
}
</script>

<template>

<!-- HEADER -->
  <Header />

<!-- SLIDER REVIEWS -->
  <SliderReviews />


<!-- FOOTER -->
  <Footer />


</template>

<!-- SCSS -->
<style lang="scss">

// STILI GENERALI
@use "./scss/main.scss";

</style>