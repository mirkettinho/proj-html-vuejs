<script>


export default {
  name: "Dropdown",
  props:[
    "list"
  ],
  data(){
    return{

    }
  }
}
</script>

<template>
  <ul v-show="list.open" id="sub-items">
      <li class="sub-item" v-for="(link,index) in list.subnav" :key="index">
        <a  @click="link.open = !link.open" :href="link.href">{{ link.title }}</a>
        <i v-if="link.subnav" :class="{'fa-solid fa-chevron-down' : !link.open, 'fa-solid fa-chevron-up' : link.open}"></i>
        <Dropdown v-if="link.subnav" :list="link"/>
      </li>
    </ul>
</template>

<style lang="scss" scoped>
#sub-items{
  list-style: none;
}
ul{
  margin-top: 20px;
}li{
  
    a{
      font-size: 0.83rem;
      cursor: pointer;
      text-decoration: none;
      color: black;
      background-color: white;
      
      &:hover{
        background-color: #f6f6f6;
      }
      
    }
  }
</style>