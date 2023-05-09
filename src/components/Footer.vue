<script>
import {footerMenu} from "../data/menus"


export default {
  name: "Footer",
  data(){
    return{
      footerMenu
    }
  }
}
</script>

<template>
  <footer>

  </footer>
  <div class="footer-bottom">
    <h5>© Copyright 2012 - 2023 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</h5>
    <img src="/img/payment_cards_footer.png" alt="">
  </div>
</template>

<style lang="scss" scoped>
.footer-bottom{
  height: 150px;
  background-color: #1e2124;
  color: #f5f5f5;
  text-align: center;
  h5{
    padding-top: 40px;
    padding-bottom: 20px;
  }
}
</style>