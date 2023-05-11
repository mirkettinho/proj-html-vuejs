
<script>
import {footerMenu} from "../../data/menus"


export default {
  name: "RecentPosts",
  
  data(){
    return{
      footerMenu
    }
  }
}
</script>

<template>
  <div class="card" v-for="(post,index) in footerMenu.recentPosts" :key="index">
    <div class="card-header" @click="post.open = !post.open">
      
      <a :class="{'active' : post.open}"><i  :class="{'fa-solid fa-chevron-down' : !post.open, 'fa-solid fa-chevron-up' : post.open}"></i>{{ post.title }}</a>
      
    
    <div v-show="post.open" class="card-content">
      {{ post.content }}
    </div>
  </div>
    <div class="bottom"></div>

  </div>

</template>

<style lang="scss" scoped>

@use "../../scss/partial/colors" as *;

.card{
  width: 92%;
  display: block;
  position: relative;
  padding: 0 10px;
}.card-header{
  padding: 10px 0;
  font-size: 0.8rem;
  a{
    cursor: pointer;
    &:hover{
      color: $star-button-and-hoverlink;
    }
    i{
      font-size: 10px;
      padding-right: 8px;
    }
  }
}.bottom{
  border-bottom: 1px solid #34373b;

}.card-content{
      margin-left: 19px;
      padding-top: 5px;
    }.active{
      color: $star-button-and-hoverlink;
    }
    
</style>