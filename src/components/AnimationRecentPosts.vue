
<script>
import RecentPosts from ".//RecentPosts.vue"

export default {
  name: "AnimationRecentPosts",
  components: {
    RecentPosts
  },
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
  <RecentPosts />
</transition>

</template>

<style lang="scss" scoped>
.expand-enter-active, .expand-leave-active {
    transition: height .5s ease-in-out;
    overflow: hidden;
  }
</style>