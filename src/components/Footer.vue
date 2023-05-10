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
  
  <!-- FOOTER -->
  <footer id="footer"> 
    <div class="top container">

      <!-- COL 1 -->
      <div class="col">
        
      </div>
      <!-- col 2 -->
      <div class="col">
        2
      </div>
      <!-- COL 3  -->
      <div class="col">
        3
      </div>
      <!-- COL 4 -->
      <div class="col">
        4
      </div>
    </div>
  </footer>
  
  <!-- FOOTER BOTTOM -->
  <div class="footer-bottom">
    <h5>© Copyright 2012 - 2023 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</h5>
    <img src="/img/payment_cards_footer.png" alt="">
  </div>
</template>

<style lang="scss" scoped>

@use "../scss/partial/colors" as *;
@use "../scss/partial/general" as *;


#footer{
  background-color: $footer-color;
  color: white;
  .top{
    display: flex;
    
  }
  .col{
    background-color: green;
    width: 25%;
    
  }
}
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