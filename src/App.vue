<template>
  <div id="app">
    <MyHeader :navbarOptions="navbarOptions"/>
    <MyMain/>
    <MyFooter :footerNavbarOptions="footerNavbarOptions" :onlineOrder="onlineOrder" :generalInfo="generalInfo" :openingHours="openingHours"/>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader.vue"
import MyMain from "./components/MyMain.vue"
import MyFooter from "./components/MyFooter.vue"

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter
  },
  data(){
    return{
      navbarOptions:['Home <i class="fa-solid fa-chevron-down"></i>', "Order Online", "About", "News", "Contact Us", '<i class="fa-solid fa-cart-shopping"></i>'],
      footerNavbarOptions:['<span class="highlighted">Home</span>', "Order Online", "About", "News", "Contact Us", 'Cart'],
      onlineOrder:['Appetizers', 'Burgers', 'Pizza', 'Fries', 'Sides', 'Desserts', 'Beverages', 'Specials'],
      generalInfo:['My Account', 'Terms Of Service', 'Privacy Policy'],
      openingHours:['Mon - <span class="highlighted">10 AM to 11PM</span>', 'Tue - <span class="highlighted">10 AM to 11PM</span>', 'Wed - <span class="highlighted">10 AM to 11PM</span>', 'Thur - <span class="highlighted">10 AM to 11PM</span>', 'Fri - <span class="highlighted">10 AM to 11PM</span>', 'Sat - <span class="highlighted">10 AM to 11PM</span>', 'Sun - <span class="highlighted">10 AM to 11PM</span>', ]
    }
  }
}
</script>

<style lang="scss">
  @import "./assets/scss/common.scss";
</style>
