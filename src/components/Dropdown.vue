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
        <a @click="link.open = !link.open" :href="link.href">{{ link.title }}</a>
        <i v-if="link.subnav" :class="{'fa-solid fa-caret-down' : !link.open, 'fa-solid fa-caret-up' : link.open}"></i>
        <Dropdown v-if="link.subnav" :list="link"/>
      </li>
    </ul>
</template>

<style lang="scss" scoped>

</style>