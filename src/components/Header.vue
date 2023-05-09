
<script>
import Dropdown from "../components/Dropdown.vue"
import {headerMenu} from "../data/menus"

export default {
  name: "Header",
  components: {
    Dropdown,
    
  },
  data(){
    return{
      headerMenu
    }
  }
}
</script>

<template>
    <div class="top">
      <div class="container">
        <div class="social">
          <a href="https://www.facebook.com/" target="blank"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="https://twitter.com/login?lang=it" target="blank"><i class="fa-brands fa-twitter"></i></a>
          <a href="https://www.instagram.com/" target="blank"><i class="fa-brands fa-instagram"></i></a>
          <a href="https://www.youtube.com/" target="blank"><i class="fa-brands fa-youtube"></i></a>
        </div>
        <div class="info-shopping">
          <a href="#">Shopping Cart</a>
          <a href="#">My Account</a>
          <a href="#"><i class="fa-sharp fa-solid fa-bag-shopping"></i>Cart</a>
        </div>
      </div>
    </div>
    <div id="header" class="container">
      <ul id="link">
        <div class="logo">
          <img src="../../public/img/classic_shop_logo1x.png" alt="">
        </div>
        <li  v-for="(link,index) in headerMenu.links" :key="index">
          <a :class="{'active' : link.isActive}" @click="link.open = !link.open" :href="link.href">{{ link.title }}</a>
          <i v-if="link.subnav" :class="{'fa-solid fa-chevron-down' : !link.open, 'fa-solid fa-chevron-up' : link.open}"></i>
          <Dropdown v-if="link.subnav" :list="link"/>
        </li>
      </ul>
        <a class="btn blue ">SHOP NOW!</a>

        <div>
          <i class="fa-solid fa-magnifying-glass fa-beat"></i>
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use "../scss/partial/colors" as *;

.top{
  height: 40px;
  background-color: white;
  border-bottom: 1px solid #eaeaea;
  border-top: 3px solid $star-button-and-hoverlink;
}
#header{
  height: 90px;
  background-color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;

  
}#link{
  list-style: none;
  display: flex;
  align-items: center;
  
  li{
      padding: 20px;
    a{
      font-size: 0.83rem;
      cursor: pointer;
      &:hover,
      &.active{
        color: $star-button-and-hoverlink;
      }
    }
  }
  }i{
    padding-left: 5px;
    font-size: 9px;
  }.btn.blue{
    background-color: $star-button-and-hoverlink;
    padding: 10px 20px;
    border-radius: 20px;
    color: $primary-color;
    
  }

</style>