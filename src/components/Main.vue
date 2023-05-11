
<script>
import BrandLogo from "./micro-components/BrandLogo.vue"
import MiniShowcase from "./micro-components/MiniShowcase.vue"
import FromOurBlog from "./micro-components/FromOurBlog.vue"
import Testimonials from "./micro-components/Testimonials.vue"
import NewArrivals from "./micro-components/NewArrivals.vue"
import Promo from "./micro-components/Promo.vue"
import BestSeller from "./micro-components/BestSeller.vue"
import Collections from "./micro-components/Collections.vue"



export default {
  name: "Main",
  components: {
    Collections,
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


  <!-- COLLECTIONS -->
  <Collections />

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