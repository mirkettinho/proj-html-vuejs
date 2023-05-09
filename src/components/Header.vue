
<script>
import Dropdown from "../components/Dropdown.vue"
import {headerMenu} from "../data/menus"

export default {
  name: "Header",
  components: {
    Dropdown,
    
  },
  data(){
    return{
      headerMenu
    }
  }
}
</script>

<template>
  <div id="header">
    <div class="logo">
      <img src="../../public/img/classic_shop_logo1x.png" alt="">
    </div>
    <ul id="link">
      <li v-for="(link,index) in headerMenu.links" :key="index">
        <a @click="link.open = !link.open" :href="link.href">{{ link.title }}</a>
        <i v-if="link.subnav" :class="{'fa-solid fa-caret-down' : !link.open, 'fa-solid fa-caret-up' : link.open}"></i>
        <Dropdown v-if="link.subnav" :list="link"/>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
#header{
  height: 50px;
  background-color: greenyellow;
}
</style>