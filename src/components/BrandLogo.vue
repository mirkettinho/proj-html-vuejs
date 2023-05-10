
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/free-mode';
import 'swiper/css/pagination';

import { Pagination, Navigation} from 'swiper';


export default {
  name: "BrandLogo",
  components: {
      Swiper,
      SwiperSlide,
    },
    data(){
      return{

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
      <h5 >BRAND LOGO</h5>
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

      
      <swiper-slide class="">
        <div class="">
          <div class="card">
            <img src="/img/brands/b_logotype_1.png" alt="">
          </div>
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="card">
          <img src="/img/brands/b_logotype_2.png" alt="">
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="card">
          <img src="/img/brands/b_logotype_3.png" alt="">
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="card">
          <img src="/img/brands/b_logotype_4.png" alt="">
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="card">
          <img src="/img/brands/b_logotype_5.png" alt="">
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="card">
          <img src="/img/brands/b_logotype_6.png" alt="">
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="card">
          <img src="/img/brands/b_logotype_7.png" alt="">
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