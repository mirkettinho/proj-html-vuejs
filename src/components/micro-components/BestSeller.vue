
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Autoplay, Pagination, Navigation } from 'swiper';
import {BestSeller} from "../../data/sliderMain"


export default {
  name: "BestSeller",
  components: {
    Swiper,
    SwiperSlide
  },
  data(){
    return{
      BestSeller
    }
  },
  setup() {
      return {
        modules: [Autoplay, Pagination, Navigation],
      };
    },
}
</script>

<template>

  <div class="container">

    <div class="title d-flex align-items justify-content">
        <div class="bottom"></div> 
          <h1>Best Seller</h1>
        <div class="bottom"></div>
    </div>

      <div class="second-title" >
        <h5>Must have products from our top sellers</h5>
      </div>

      <swiper
    :slidesPerView="5"
    :spaceBetween="0"
    :centeredSlides="true"
    :loop="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    
    :navigation="true"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide v-for="(seller, index) in BestSeller.sellers" :key="index">
      
    <!-- CARD -->
    <div class="card">
      <img :src="seller.image" alt="">
    </div>

    </swiper-slide>

    

      

  </swiper>
  </div>


</template>


<style lang="scss" scoped>
@import "swiper/swiper.css";
@import "../../scss/partial/general";

.card{
  height: 400px;
  background-color: white;
  
  img{
    height:  300px;
  }
}
.second-title{
  text-align: center;
  color: #5f615f;
  padding-bottom: 20px;
}

.bottom{
  width: 36%;
  height: 2px;
  background-color: #eaeaea;
  margin-right: 20px;
}

.title{
  margin: 0px 20px;
  padding-bottom: 10px;
  padding-top: 90px;
  
}
</style>