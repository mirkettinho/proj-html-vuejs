<script>
import {footerMenu} from "../data/menus"
import RecentPosts from "./micro-components/RecentPosts.vue"
import Newsletter from "./micro-components/Newsletter.vue"

export default {
  name: "Footer",
  components: {
    RecentPosts,
    Newsletter
  },
  data(){
    return{
      footerMenu
    }
  }
}
</script>

<template>

  <Newsletter />
  <!-- FOOTER -->
  <footer id="footer"> 
    <div class="top container">

      <!-- COL 1 -->
      <!-- CONTACTS -->
      <div class="col">
        <img class="logo" src="img/logo/classic_shop_logo_footer.png" alt="">

        <div class="contact">
          <span>12345 North Main Street,</span>
          <span>New York, NY 555555</span>
          <span>Phone: 1.800.555.6789</span>
          <span>Email: info@company.com</span>
          <span>Web: Theme-fusion.com</span>
        </div>

        <div class="social ">
          <a href="https://www.facebook.com/" target="blank"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="https://twitter.com/login?lang=it" target="blank"><i class="fa-brands fa-twitter"></i></a>
          <a href="https://www.instagram.com/" target="blank"><i class="fa-brands fa-instagram"></i></a>
          <a href="https://www.youtube.com/" target="blank"><i class="fa-brands fa-youtube"></i></a>
        </div>
      </div>

      <!-- col 2 -->
      <!-- TOP RATED PRODUCTS -->
      <div class="col product">
        <h5>TOP RATED PRODUCTS</h5>
        <div class="single-card" v-for="(rated,index) in footerMenu.topRated" :key="index">

          <div class="box-card d-flex justify-content">
            <div class="description-card">
              <a href="">{{ rated.name }}</a>
              <h6>{{ rated.rating }}</h6>
              <h6>{{ rated.discount }} {{ rated.price }}</h6>
            </div>

            <div class="image-card">
              <img :src="rated.image" alt="">
            </div>
          </div>
          
          <div class="bottom"></div>
        </div>
      </div>

      <!-- COL 3  -->
      <!-- RECENT POSTS -->
      <div class="col">
        <h5>RECENT POSTS</h5>
        <RecentPosts />
      </div>

      <!-- COL 4 -->
      <!-- TAGS -->
      <div class="col last">
        <h5>TAGS</h5>
        <div class="tags d-flex wrap" >
          <span v-for="(tag,index) in footerMenu.tags" :key="index">{{ tag.text }}</span>
        </div>
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
  color: $footer-text-color;
  padding-top: 50px;
  padding-bottom: 25px;
  .top{
    display: flex;
    
  }
  .col.product{
  width: 21%;
}
  .col.last{
    width: 20%;
  }
  .col{
    margin: 0 auto;
    width: 25%;
    h5{
      padding-bottom: 20px;
    }.tags span{
      padding: 4px 10px;
      margin: 1px;
      border: 1px solid #34373b;
      font-size: 0.7rem;
      &:hover{
        background-color: $hover-tags;
        color: white;
        cursor: pointer;
      }
    }.image-card img{
      height: 55px;
      margin-right: 20px;
    }
    .logo{
      width: 160px;
      padding-bottom: 40px;
    }.contact{
      padding-bottom: 40px;
      span{
      display: flex;
      font-size: 0.7rem;
      padding: 5px 0;
    }
  }
    .social a{
    padding: 6px;
    i{
      font-size: 10px;
      color: $footer-social;
    }
  }
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
}.bottom{
  border-bottom: 1px solid #34373b;
  margin-right: 20px;
}.box-card{
  padding: 10px 0;
}

.description-card{
  a{
    color: white;
    font-size: 0.7rem;
    &:hover{
      color: $star-button-and-hoverlink;
    }
  }
}


</style>