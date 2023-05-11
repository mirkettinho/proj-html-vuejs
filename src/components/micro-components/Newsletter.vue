
<script>


export default {
  name: "Newsletter",
  data(){
    return{

    }
  }
}
</script>

<template>
  <div class="newsletter">
    
    <div class="container ">
      <div class="newsletter-content d-flex align-items">
        <div class="d-flex align-items">
          <i class="fa-sharp fa-regular fa-envelope fa-bounce "></i>
          <h3>Subscribe now and get special offers</h3>
        </div>
        <div >
          <input type="email" class="filter" placeholder="Insert your email">
          <button>SEND</button>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

@use "../../scss/partial/colors" as *;

.newsletter{
  background-color: #2e3238;
  .newsletter-content{
    padding: 70px 0;
    i{
      font-size: 30px;
      color: #74797d;
      background-color: $footer-color;
      padding: 15px;
      border-radius: 50%;
      margin-right: 25px;
    }
    h3{
      color: white;
      margin-right: 100px;
      font-size: 1.6rem;
    }
    input{
      padding: 10px 50px;
      border-radius: 20px;
      border: none;
      font-size: 0.7rem;
      margin-right: 20px;
      &:focus{
        outline: none;
      }
    }.filter{
      padding: 10px 80px 10px 10px;
    }
    
    button{
      color: white;
      background-color: $star-button-and-hoverlink;
      padding: 10px 40px;
      border-radius: 20px;
      border: none;
      font-weight: 700;

    }
  }
}
</style>