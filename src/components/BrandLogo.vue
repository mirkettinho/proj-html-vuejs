
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/free-mode';
import 'swiper/css/pagination';
import {sliderBrandLogo} from "../data/sliderMain"

import { Pagination, Navigation} from 'swiper';


export default {
  name: "BrandLogo",
  components: {
      Swiper,
      SwiperSlide,
    },
    data(){
      return{
        sliderBrandLogo
      }
    },
    setup() {
      return {
        modules: [Pagination, Navigation],
      };
    },
}
</script>

<template>
  <div class="bg">
    <div class="brand container">
      <h5 v-for="(brand, index) in sliderBrandLogo.title" :key="index">{{brand.name}}</h5>
    </div>
  </div>

  <div class="bg">
    <swiper
      :slidesPerView="5"
      :spaceBetween="0"
      :loop="true"
      :navigation="true"
      :modules="modules"
      class="mySwiper container">

      
      <swiper-slide  v-for="(brand, index) in sliderBrandLogo.brands" :key="index">

        
          <div class="card">
          <a :href="brand.href"><img :src="brand.image" alt=""></a>
          </div>
      </swiper-slide>

    </swiper>
  </div>
</template>


<style lang="scss" scoped>

@import "swiper/swiper.css";
@import "../scss/partial/general";

.brand{
  text-align: center;
  padding: 40px 0;
}
.bg{
  background-color: #f6f6f6;
}
.card{
  height: 200px;
  img{
    height: 120px;
    padding-left: 60px;
    
  }
}

</style>