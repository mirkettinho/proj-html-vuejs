
<script>





export default {
  name: "SliderReviews",
  
  data(){
    return{

    }
  },
  setup() {
      return {
        
      };
    },
}
</script>

<template>
  <swiper
    :spaceBetween="30"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide></swiper-slide>
  </swiper>
</template>

<style lang="scss" scoped >

</style>