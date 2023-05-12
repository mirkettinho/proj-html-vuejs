
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
      <div class="description">
        <h2>{{arrival.title}}</h2>
        <h3>{{arrival.type}}</h3>
        <span>{{arrival.price}}</span>
        <div class="button d-flex ">
          <a href="#"><i class="fa-solid fa-cart-plus fa-shake"></i>{{arrival.shop}}</a>
          <a href="#"><i class="fa-solid fa-list-ul"></i>{{arrival.details}}</a>
        </div>
      </div>
    </div>

    </swiper-slide>
    <div class="bg-white"></div>
  </swiper>

</template>

<style lang="scss" scoped>

@import "swiper/swiper.css";
@import "../../scss/partial/general";


.card{
  height: 420px;
  background-color: white;
  position: relative;
  &:hover .description{
    opacity: 1;
    height: 100%;
  }

  
  img{
    height:  420px;  
  }.description{
    position: absolute;
    overflow: hidden;
    background: linear-gradient(rgba(111, 141, 212,0.9), rgba(232, 164, 209,1.1));
    height: 0;
    width: 100%;
    opacity: 0;
    bottom: 0;
    transition: 0.3s ease;
    h2{
    text-align: center;
    line-height: 340px;
    color: white;
    font-size: 1.5rem;
    }h3{
      left: 25%;
      top:50px;
      position: absolute;
      line-height: 340px;
      font-size: 0.9rem;
      color: white;

    }
    span{
      top:50px;
      left: 40%;
      text-align: center;
      position: absolute;
      line-height: 340px;
      color: white;
      font-size:  1.5rem;

    }span{
      top: 100px;
      left: 41%;
    }
    .button{
      justify-content: space-evenly;
      a{
        color: white;
        font-size: 0.9rem;
        i{
          padding-right: 5px;
        }
      }

    }
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

.bg-white{
  height: 140px;
}


</style>