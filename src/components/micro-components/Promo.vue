
<script>

import {Promos} from "../../data/sliderMain"


export default {
  name: "Promo",
  data(){
    return{
      Promos
    }
  }
}
</script>

<template>
  <div class="bg">
    <div class="d-flex justify-content align-items container">
      
      <div class="box" v-for="(box, index) in Promos.promo" :key="index">
        <img src="img/promo_box/promo_box_1_bg.jpg" alt="">
          <h1>{{box.title}}</h1>
          <p>{{box.content}}</p>
          <a :href="box.href">{{box.namebutton}}</a>
      </div>


    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../../scss/partial/general";

.bg{
  
  background-image: url("img/background/bkgd_confetti-compressor.jpg");
  background-position: center;
  background-size: cover;
  margin-top: 90px;
}

.box{
  position: relative;
  padding: 40px 10px;
  
  
  img{
    width: 430px;
  } 
  h1{
    position: absolute;
    top: 120px;
    left: 40px;
    color: white;
  }p{
    position: absolute;
    left: 40px;
    top: 170px;
    width: 200px;
    font-size: 0.8rem;
    line-height: 20px;
    color: white;

  }a{
    position: absolute;
    bottom: 105px;
    left: 40px;
    padding: 10px 18px;
    border: 1px solid white;
    border-radius: 20px;
    color: white;
    font-size: 0.6rem;
    &:hover{
      background-color: rgba(0, 0, 0, 0.1)  ;
    }
  }
}
</style>