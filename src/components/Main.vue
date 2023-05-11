
<script>
import BrandLogo from "./micro-components/BrandLogo.vue"
import MiniShowcase from "./micro-components/MiniShowcase.vue"
import FromOurBlog from "./micro-components/FromOurBlog.vue"


export default {
  name: "Main",
  components: {
    FromOurBlog,
    MiniShowcase,
    BrandLogo
  }
}
</script>

<template>
  


  <!-- FROM OUR BLOG -->
  <FromOurBlog />

  <!-- MINI SHOWCASE -->
  <MiniShowcase />

  <!-- BRAND LOGOS -->
  <BrandLogo />

</template>

<style>

</style>