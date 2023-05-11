
<script>
import BrandLogo from "./micro-components/BrandLogo.vue"
import MiniShowcase from "./micro-components/MiniShowcase.vue"
import FromOurBlog from "./micro-components/FromOurBlog.vue"
import Testimonials from "./micro-components/Testimonials.vue"


export default {
  name: "Main",
  components: {
    Testimonials,
    FromOurBlog,
    MiniShowcase,
    BrandLogo
  }
}
</script>

<template>
  

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