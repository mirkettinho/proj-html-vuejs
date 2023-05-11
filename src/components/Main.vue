
<script>
import BrandLogo from "./micro-components/BrandLogo.vue"
import MiniShowcase from "./micro-components/MiniShowcase.vue"
import FromOurBlog from "./micro-components/FromOurBlog.vue"
import Testimonials from "./micro-components/Testimonials.vue"
import NewArrivals from "./micro-components/NewArrivals.vue"
import Promo from "./micro-components/Promo.vue"
import BestSeller from "./micro-components/BestSeller.vue"



export default {
  name: "Main",
  components: {
    BestSeller,
    Promo,
    NewArrivals,
    Testimonials,
    FromOurBlog,
    MiniShowcase,
    BrandLogo
  }
}
</script>

<template>

  <!-- BEST SELLER -->
  <BestSeller />

  <!-- PROMO -->
  <Promo />

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