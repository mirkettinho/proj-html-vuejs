
<script>
import Dropdown from "./micro-components/Dropdown.vue"
import {headerMenu} from "../data/menus"



export default {
  name: "Header",
  components: {
    Dropdown,
    
  },
  data(){
    return{
      headerMenu,

    }
  }
}
</script>

<template>
    <div class="top d-flex">
      <div class="container d-flex justify-content align-items">

        <!-- SOCIAL -->
        <div class="social ">
          <a href="https://www.facebook.com/" target="blank"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="https://twitter.com/login?lang=it" target="blank"><i class="fa-brands fa-twitter"></i></a>
          <a href="https://www.instagram.com/" target="blank"><i class="fa-brands fa-instagram"></i></a>
          <a href="https://www.youtube.com/" target="blank"><i class="fa-brands fa-youtube"></i></a>
        </div>

        <!-- SHOPPING -->
        <div class="info-shopping d-flex align-items">         
          <a href="#">Shopping Cart</a>         
          <a class="border" href="#">My Account</a>
          <a href="#"><i class="fa-sharp fa-solid fa-bag-shopping"></i>CART<i class="fa-solid fa-chevron-down"></i></a>
        </div>
      </div>
    </div>

    <!-- HEADER LOGO + LINKS -->
    <div id="header" class="container">
      <div class="logo" id="home">
        <img src="/img/logo/classic_shop_logo1x.png" alt="">
      </div>
      <ul id="link">
        <li  v-for="(link,index) in headerMenu.links" :key="index">
          <a :class="{'activee' : link.isActive, 'active' : link.open}" @click="link.open = !link.open" :href="link.href">{{ link.title }}<i v-if="link.subnav" :class="{'fa-solid fa-chevron-down' : !link.open, 'fa-solid fa-chevron-up' : link.open}"></i></a>
          <Dropdown v-if="link.subnav" :list="link"/>
        </li>
        <a class="btn blue ">SHOP NOW!</a>
        <i class="fa-solid fa-magnifying-glass fa-beat"></i>
      </ul>

        
    

    </div>
</template>


<style lang="scss" scoped>
@use "../scss/partial/colors" as *;
@use "../scss/partial/general" as *;
  .social a{
    padding: 6px;
    i{
      font-size: 10px;
      color: $icon-header;
      &:hover{
        color: $star-button-and-hoverlink;
      }

    }
  }
  .info-shopping a{
    padding: 10px;
    font-size: 10px;
    color: black;
    i{
      padding-right: 5px;
    }
  }.info-shopping a:last-child{
    padding: 9px 30px;
    background-color: #f2f2f2;
  }.border{
    border: 1px solid #eaeaea;

  }


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
      position: relative;
      
      &:hover:after{
        width: 100%;
        
      }
      &:after{
        content: "";
        position: absolute;
        background-color: $star-button-and-hoverlink;
        height: 4px;
        width: 0;
        left: 0;
        bottom: 49px;
        transition: 0.4s ;
      }
      &:hover,
      &.active,
      &.activee{
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
    margin-right: 30px;
    margin-left: 15px;
    font-size: 10px;
    
  }

</style>