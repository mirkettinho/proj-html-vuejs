
<script>
import BrandLogo from "./micro-components/BrandLogo.vue"
import MiniShowcase from "./micro-components/MiniShowcase.vue"

export default {
  name: "Main",
  components: {
    MiniShowcase,
    BrandLogo
  }
}
</script>

<template>
  
  <!-- MINI SHOWCASE -->
  <MiniShowcase />


  <!-- BRAND LOGOS -->
  <BrandLogo />

</template>

<style>

</style>