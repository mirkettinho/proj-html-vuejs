
<script>
import BrandLogo from "./micro-components/BrandLogo.vue"
import MiniShowcase from "./micro-components/MiniShowcase.vue"
import FromOurBlog from "./micro-components/FromOurBlog.vue"
import Testimonials from "./micro-components/Testimonials.vue"
import NewArrivals from "./micro-components/NewArrivals.vue"


export default {
  name: "Main",
  components: {
    NewArrivals,
    Testimonials,
    FromOurBlog,
    MiniShowcase,
    BrandLogo
  }
}
</script>

<template>
  

  <!-- NEW ARRIVALS -->
  <NewArrivals />

  <!-- TESTIMONIALS -->
  <Testimonials />

  <!-- FROM OUR BLOG -->
  <FromOurBlog />

  <!-- MINI SHOWCASE -->
  <MiniShowcase />

  <!-- BRAND LOGOS -->
  <BrandLogo />

</template>

<style>

</style>