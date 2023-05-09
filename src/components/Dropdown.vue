<script>


export default {
  name: "Dropdown",
  props:[
    "list"
  ],
  data(){
    return{

    }
  }, 
  methods: {
      enter(el) {
        el.style.height = 'auto';
        const height = getComputedStyle(el).height;
        el.style.height = 0;
        getComputedStyle(el);

        setTimeout(() => {
          el.style.height = height;
        });        
      },
      afterEnter(el) {
        el.style.height = 'auto';
      },
      leave(el) {
        el.style.height = getComputedStyle(el).height;

        getComputedStyle(el);

        setTimeout(() => {
          el.style.height = 0;
        });
      }
    }
  }

</script>

<template>
  <transition 
    name="expand"
    @enter="enter"
    @after-enter="afterEnter"
    @leave="leave">
    <ul v-show="list.open" id="sub-items">
        <li class="sub-item" v-for="(link,index) in list.subnav" :key="index">
          <a  @click="link.open = !link.open" :href="link.href">{{ link.title }}</a>
          <i v-if="link.subnav" :class="{'fa-solid fa-chevron-down' : !link.open, 'fa-solid fa-chevron-up' : link.open}"></i>
          <Dropdown v-if="link.subnav" :list="link"/>
        </li>
      </ul>
    </transition>
</template>

<style lang="scss" scoped>
#sub-items{
  list-style: none;
  position: absolute;
  top: 120px;
}li{
  background-color: white;
  padding: 10px;
    &:hover{
      background-color: #f6f6f6;
      cursor: pointer;
    }
    a{
      font-size: 0.83rem;
      cursor: pointer;
      text-decoration: none;
      color: black;
      
      }
      
    }
    .expand-enter-active, .expand-leave-active {
    transition: height .5s ease-in-out;
    overflow: hidden;
  }
</style>