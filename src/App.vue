<template>
  <div id="app">
    <MyHeader :navbarOptions="navbarOptions"/>
    <MyMain/>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue"
import MyMain from "./components/MyMain.vue"

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  data(){
    return{
      navbarOptions:['Home <i class="fa-solid fa-chevron-down"></i>', "Order Online", "About", "News", "Contact Us", '<i class="fa-solid fa-cart-shopping"></i>'],
    }
  }
}
</script>

<style lang="scss">
  @import "./assets/scss/common.scss";
</style>
