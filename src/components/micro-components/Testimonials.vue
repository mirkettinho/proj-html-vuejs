
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';

import "swiper/css/effect-fade";
import {Testimonials} from "../../data/sliderMain"


import { Autoplay, EffectFade, Pagination, } from 'swiper';



export default {
  name: "Testimonials",
  components: {
    Swiper,
    SwiperSlide
  },
  data(){
    return{
      Testimonials
    }
  },
  setup() {
      return {
        modules: [ Autoplay, EffectFade, Pagination,],
      };
    },
}

</script>

<template>
  <swiper
    :spaceBetween="0"
    :effect="'fade'"
    :loop="true"
    :autoplay="{
      delay: 5000,
      disableOnInteraction: false,
      }"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide v-for="(testimonial, index) in Testimonials.article" :key="index">
      <div class="bg">

        <div class="card container d-flex justify-content align-items">
          <div class="pd-bottom">
            <img :src="testimonial.image" alt="">
          </div>
          <p>{{ testimonial.content }}</p>

          <div class="credits">
            <span class="bold">{{testimonial.credits}}</span>, <span>{{testimonial.creditsTwo}}</span>
          </div>
        </div>

      </div>
    </swiper-slide>

    
  </swiper>
</template>

<style lang="scss" scoped>
@import "swiper/swiper.css";
@import "../../scss/partial/general";

.bg{
  background-image: url("img/testimonial/testimonials_home_1_bg.jpg");
  background-position: center;
  background-size: cover;
  
  img{
    height: 80px;
    
  }
}

.card{
  flex-direction: column;
  padding-top: 80px;
  color: white;
  p{
    margin: 0px 50px;
    padding-bottom: 20px;
    font-size: 0.9rem;
    line-height: 25px;

  }
  .credits{
    padding-bottom: 120px;
    span{
      font-size: 0.9rem;
    }
  }
}

.pd-bottom{
  padding-bottom: 20px;
}


.bold{
  font-weight: 700;
}
</style>