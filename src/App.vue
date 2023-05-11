
<script>
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"
import Main from "./components/Main.vue"


export default {
  name: "App",
  components: {
    Header,
    Footer,
    Main
  }
}
</script>

<template>

<!-- HEADER -->
  <Header />

<!-- MAIN -->

  <Main />
<!-- FOOTER -->
  <Footer />


</template>

<!-- SCSS -->
<style lang="scss">

// STILI GENERALI
@use "./scss/main.scss";

</style>