
<script>
import {SectionMiniShowcase} from "../../data/sliderMain"


export default {
  name: "MiniShowcase",
  data(){
    return{
      SectionMiniShowcase
    }
  }
}
</script>

<template>
  
  <div class="top"></div>

  <div class="container">

    <div class="d-flex">
    
    <!-- col 1 -->
      <!-- FEATURED -->
        <div class="col product">
          <h5>FEATURED</h5>
          <div class="single-card" v-for="(featured,index) in SectionMiniShowcase.featureds" :key="index">

            <div class="box-card d-flex justify-content">
              <div class="description-card">
                <a href="#">{{ featured.name }}</a>
                <h6>{{ featured.rating }}</h6>
                <h6>{{ featured.discount }} {{ featured.price }}</h6>
              </div>

              <div class="image-card">
                <img :src="featured.image" alt="">
              </div>
            </div>
            
            <div class="bottom"></div>
          </div>
        </div>
    


    <!-- col 2 -->
      <!-- ON SALE -->   
        <div class="col product">
          <h5>ON SALE</h5>
          <div class="single-card" v-for="(sale,index) in SectionMiniShowcase.onSales" :key="index">

            <div class="box-card d-flex justify-content">
              <div class="description-card">
                <a href="#">{{ sale.name }}</a>
                <h6>{{ sale.rating }}</h6>
                <h6>{{ sale.discount }} {{ sale.price }}</h6>
              </div>

              <div class="image-card">
                <img :src="sale.image" alt="">
              </div>
            </div>
            
            <div class="bottom"></div>
          </div>
        </div>



    <!-- col 3 -->
      <!-- TOP RATED -->    
        <div class="col product">
          <h5>TOP RATED</h5>
          <div class="single-card" v-for="(rated,index) in SectionMiniShowcase.topRated" :key="index">

            <div class="box-card d-flex justify-content">
              <div class="description-card">
                <a href="#">{{ rated.name }}</a>
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



    <!-- col 1 -->
      <!-- LATEST REVIEWS -->
        <div class="col product">
          <h5>LATEST REVIEWS</h5>
          <div class="single-card" v-for="(review,index) in SectionMiniShowcase.latestReviews" :key="index">

            <div class="box-card d-flex justify-content">
              <div class="description-card">
                <a href="#">{{ review.name }}</a>
                <h6>{{ review.rating }}</h6>
                <h6>{{ review.discount }} {{ review.price }}</h6>
              </div>

              <div class="image-card">
                <img :src="review.image" alt="">
              </div>
            </div>
            
            <div class="bottom"></div>
          </div>
        </div>

        






    </div>
  </div>
</template>

<style lang="scss" scoped>

@use "../../scss/partial/colors" as *;
@import "../../scss/partial/general";


.col.product{
  width: 21%;
  margin: 0 auto;
  margin: 40px auto;
  h5{
    padding: 15px 0;
    color: #5f615f;
  }
}

.description-card{
  a{
    color: #5f615f;
    font-size: 0.7rem;
    &:hover{
      color: $star-button-and-hoverlink;
    }
  }
}

.bottom{
  border-bottom: 1px solid #eaeaea;
  margin-right: 20px;
}.box-card{
  padding: 3px 0;
}

.image-card img{
      height: 55px;
      margin-right: 20px;
    }

.top{
  border-bottom: 1px solid #eaeaea;
  margin-right: 20px;
  width: 98%;
  margin: 0 auto;
}
</style>