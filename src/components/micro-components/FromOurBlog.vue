
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
    <div class="title d-flex align-items justify-content">
      <div class="bottom"></div> 
        <h1>From Our Blog</h1>
      <div class="bottom"></div>
    </div>

    <!-- SECOND-TITLE -->
    <div class="second-title">
      <h5>The latest Classic Shop news</h5>
    </div>

    <!-- CARD -->
    <div class="d-flex justify-content m-20">

      <div class="card-image m-right" v-for="(blog,index) in fromOurBlog.blogs" :key="index">
        <img :src="blog.image" alt="">

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
    padding-bottom: 15px;
  }
}

.description-card{
  h5{
    padding-bottom: 3px;
    
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