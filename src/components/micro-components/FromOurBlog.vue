
<script>
import {fromOurBlog} from "../../data/sliderMain"


export default {
  name: "FromOurBlog",
  data(){
    return{
      fromOurBlog
    }
  }
}
</script>

<template>
  <div class="container">

      <!-- TITLE -->
    <div class="title d-flex align-items justify-content" v-for="(text,index) in fromOurBlog.title" :key="index">
      <div class="bottom"></div> 
        <h1>{{text.name}}</h1>
      <div class="bottom"></div>
    </div>

    <!-- SECOND-TITLE -->
    <div class="second-title" v-for="(text,index) in fromOurBlog.subtitle" :key="index">
      <h5>{{text.name}}</h5>
    </div>

    <!-- CARD -->
    <div class="d-flex justify-content m-20">

      <div class="card-image m-right" v-for="(blog,index) in fromOurBlog.blogs" :key="index">
        <div class="image">
          <img :src="blog.image" alt="">
        </div>

        <div class="description-card">
          <h5>{{blog.name}}</h5>
          <span>{{blog.date}} | {{blog.comments}}</span>
          <p>{{blog.content}}</p>
        </div>

      </div>
    </div>

  </div>
</template>


<style lang="scss" scoped>
@use "../../scss/partial/colors" as *;
@import "../../scss/partial/general";


.m-right{
  margin-right: 20px;
}
.m-20{
  margin: 0 20px;
}
.title{
  margin: 0px 20px;
  padding-bottom: 10px;
  padding-top: 90px;
}

.second-title{
  text-align: center;
  color: #5f615f;
}
.bottom{
  width: 36%;
  height: 1px;
  background-color: #eaeaea;
  margin-right: 20px;
}


.card-image{
  padding-top: 60px;
  padding-bottom: 60px;
  width: 320px;
  
  img{
    height: 100%;
    transition: 1s ease;
    &:hover{
      height: 110%;
      filter: brightness(110%);
      
    }
  }
  
}

.image{
  width: 320px;
  height: 215px;
  overflow: hidden;
}

.description-card{
  h5{
    padding-bottom: 3px;
    padding-top: 15px;
    &:hover{
      color: $star-button-and-hoverlink;
      cursor: pointer;
    }
  }
  span{
    font-size: 0.7rem;
    color: #5f615f;
    
  }
  p{
    font-size: 0.75rem;
    color: #5f615f;
    padding-top: 15px;
    line-height: 25px;
    margin-right: 8px;
    word-spacing: 2px;
  }
}
</style>