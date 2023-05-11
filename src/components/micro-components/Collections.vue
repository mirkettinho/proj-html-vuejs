
<script>

import {Collections} from "../../data/sliderMain"


export default {
  name: "Collections",
  data(){
    return{
      Collections
    }
  }
}
</script>

<template>
  <div class="d-flex">

    <div class="col" v-for="(collection, index) in Collections.bundle" :key="index">
      <img :src="collection.image" alt="">
      <span class="absolute top">{{ collection.title }}</span>     
      <span class="absolute letter">{{collection.type}}</span>
      <a :href="collection.href" class="absolute">{{collection.namebutton}}</a>
    </div>

  </div>

</template>



<style lang="scss" scoped>

@import "../../scss/partial/general";

.col{
  margin-top: 100px;
  width: calc(100% / 3);
  height: 620px;
  overflow: hidden;
  position: relative;
  text-align: center;
  img{
    width: 640px;
    object-fit: fill;
  }.top{
    bottom: 180px;   
    color: white;
    font-size: 2.6rem;
    font-weight: bold;
    transform: translate(-50%, -50%);
    width: 400px;
    
  }span{
    bottom: 150px;   
    color: white;
    transform: translate(-50%, -50%);
    font-size: 0.95rem;

  }a{
    bottom: 75px;
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

.letter{
  letter-spacing: 5px;
}



.absolute{
  position: absolute;
}
</style>