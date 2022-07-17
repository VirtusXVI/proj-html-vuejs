<template>
  <div>
    <div class="container">
        <!-- BANNER -->
        <section class="banner">
            <div>
                <ul class="banner-content">
                    <li><i class="fa-regular fa-clock"></i>24/7 DELIVERY</li>
                    <li><i class="fa-solid fa-burger"></i>OVER 100 DISHES</li>
                    <li><i class="fa-solid fa-mobile-screen-button"></i>IN APP ORDERING</li>
                    <li><i class="fa-solid fa-car"></i>FAST DELIVERY</li>
                </ul>
            </div>
        </section>
        <!-- MAIN SECTION -->
        <section>
            <div class="main-subtitle">
                <h2>Our Most Popular Dishes</h2>
            </div>
            <div class="dishes-illustrations">
                <div class="illustration">
                    <div>
                        <img src="../assets/img/skin-on-fries.jpg" alt="fries">
                    </div>
                    <div class="illustration-text">
                        <span class="illustration-name">Skin On Fries</span>
                        <span class="illustration-price">$3.00 - $6.00</span>
                    </div>
                </div>
                <div class="illustration">
                    <div>
                        <img src="../assets/img/choco-cookie-frappe.jpg" alt="chocolate cookie frappe">
                    </div>
                    <div class="illustration-text">
                        <span class="illustration-name">Choco Cookie Frappe</span>
                        <span class="illustration-price">$4.99</span>
                    </div>
                </div>
                <div class="illustration">
                    <div>
                        <img src="../assets/img/donut-burger.jpg" alt="donut burger">
                    </div>
                    <div class="illustration-text">
                        <span class="illustration-name">The Donut Burger</span>
                        <span class="illustration-price">$6.99</span>
                    </div>
                </div>
            </div>
            <div class="button-container main-button-adjustments">
                <a href="#"><span class="button">VIEW OUR MENU <i class="fa-solid fa-circle-arrow-right"></i></span></a>
            </div>
        </section>
    </div>
    <div class="jumbotron2-background">
        <img src="../assets/material/takeout/svg-0.svg" alt="">
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    @import "../assets/scss/common.scss";
    // BANNER
    .banner{
        width: 100%;
        height: 100px;
        position: relative;
    }
    .banner div{
        position: absolute;
        top: -50px;
        height: 100%;
        width: 100%;
    }
    .banner-content{
        height: 100%;
        background-color: white;
        border: 1px solid grey;
        border-radius: 25px;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    // MAIN SECTION
    .main-subtitle h2{
        font-size: 3rem;
        text-align: center;
    }
    // DISHES
    .dishes-illustrations{
        margin-top: 4rem;
        display: flex;
        justify-content: space-between;
    }
    .illustration{
        width: calc(95% / 3);
    }
    .illustration-text span{
        display: block;
        text-align: center;
    }
    .illustration-name{
        font-size: 2rem;
        margin: 10px;
    }
    .illustration-price{
        color: $color-cube-3;
    }
    // JUMBOTRON2
    .jumbotron2-background{
        height: 800px;
        background-image: url(../assets/img/first-order-background-scaled.jpg);
        background-size: cover;
        background-repeat: no-repeat;
    }
</style>