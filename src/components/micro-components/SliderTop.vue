
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Autoplay, Pagination, Navigation } from 'swiper';
import {sliderTop} from "../../data/sliderMain"



export default {
  name: "SliderTop",
  components: {
    Swiper,
    SwiperSlide
  },
  data(){
    return{
      sliderTop
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
  <swiper
    :slidesPerView="1"
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
    <swiper-slide v-for="(slide, index) in sliderTop.jumbotron" :key="index">
      
    <!-- CARD -->
    <div class="card">
      <span class="absolute top">{{slide.title}}</span>
      <span class="absolute letter ">{{slide.type}}</span>
      <div class="d-flex">     
        <a :href="slide.href" class="absolute left">{{slide.namebuttonOne}}</a>
        <a :href="slide.href" class="absolute right">{{slide.namebuttonTwo}}</a>
      </div>
      <img :src="slide.image" alt="">
    </div>

    </swiper-slide>

  </swiper>
</template>


<style lang="scss" scoped>
@import "swiper/swiper.css";
@import "../../scss/partial/general";

.card{
  height: 700px;
  position: relative;
  text-align: center;
  
  img{
    width: 100%;
    height: 100%;
  }.top{
    bottom: 100px;
    color: white;
    font-size: 5.5rem;
    font-weight: bold;
    transform: translate(-50%, -50%);
    left: 50%;
    top: 50%;
    width: 1000px;
    
  }span{
    color: white;
    transform: translate(-50%, -50%);
    left: 50%;
    top: 50%;
    font-size: 1.5rem;
    

  }.left{
    bottom: 240px;
    left: 910px;
    color: white;
    padding: 10px 18px;
    border: 2px solid white;
    border-radius: 20px;
    color: white;
    font-size: 0.8rem;
    transform: translate(-50%, -50%);
    font-weight: bold;
    letter-spacing: 1px;
    
  }.right{
    bottom: 240px;
    left: 1050px;
    color: white;
    padding: 10px 18px;
    border: 2px solid white;
    border-radius: 20px;
    color: white;
    font-size: 0.8rem;
    transform: translate(-50%, -50%);
    font-weight: bold;
    letter-spacing: 1px;
  }
}
a:hover{
  background-color: rgba(0, 0, 0, 0.1)  ;  
      
    }

.letter{
  letter-spacing: 5px;
}

.nb{
  font-weight: 400;
}



.absolute{
  position: absolute;
}
</style>