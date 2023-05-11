
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Autoplay, Pagination, Navigation } from 'swiper';
import {NewArrivals} from "../../data/sliderMain"



export default {
  name: "NewArrivals",
  components: {
    Swiper,
    SwiperSlide
  },
  data(){
    return{
      NewArrivals
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
  
  <!-- TITLE -->

    <div class="container">

      <div class="title d-flex align-items justify-content">
        <div class="bottom"></div> 
          <h1>New Arrivals</h1>
        <div class="bottom"></div>
      </div>

      <div class="second-title" >
        <h5>Brand new products from top designers</h5>
      </div>

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
    <swiper-slide v-for="(arrival, index) in NewArrivals.arrivals" :key="index">
      
    <!-- CARD -->
    <div class="card">
      <img :src="arrival.image" alt="">
    </div>

    </swiper-slide>

  </swiper>

</template>

<style lang="scss" scoped>

@import "swiper/swiper.css";
@import "../../scss/partial/general";


.card{
  height: 480px;
  background-color: white;
  
  img{
    height:  420px;
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