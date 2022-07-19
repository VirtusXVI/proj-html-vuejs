<template>
  <div>
    <div class="container">
        <!-- BANNER -->
        <section class="banner">
            <div>
                <ul class="banner-content">
                    <li><i class="fa-regular fa-clock"></i> 24/7 DELIVERY</li>
                    <li><i class="fa-solid fa-burger"></i> OVER 100 DISHES</li>
                    <li><i class="fa-solid fa-mobile-screen-button"></i> IN APP ORDERING</li>
                    <li><i class="fa-solid fa-car"></i> FAST DELIVERY</li>
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
    <!-- JUMBOTRON 2 -->
    <div class="jumbotron2-background">
        <img src="../assets/material/takeout/svg-0.svg" alt="">
    </div>
    <div class="container">
        <!-- MENU SECTION -->
        <div class="menu-adjustments">
            <div class="main-subtitle">
                <h2>Menu Categories</h2>
            </div>
            <div class="button-container menu-button-adjustments">
                <a href="#"><span class="button">VIEW OUR MENU <i class="fa-solid fa-circle-arrow-right"></i></span></a>
            </div>
        </div>
        <div class="menu-illustrations">
            <div v-for="item,index in categories" :key="index" class="card">
                <div>
                    <img :src="getImg(categoriesImages[index])" alt="appetizer image">
                </div>
                <span>{{ item }}</span>
            </div>
        </div>
        <!-- FEATURES CARDS -->
        <div class="features-illustrations">
            <div class="features-card">
                <span class="vegetarian"><i class="fa-solid fa-leaf "></i></span>
                <span>Vegetarian</span>
            </div>
            <div class="features-card">
                <span class="glutenfree"><i class="fa-solid fa-wheat-awn"></i></span>
                <span>Gluten Free</span>
            </div>
            <div class="features-card">
                <span class="dairyfree"><i class="fa-solid fa-bottle-droplet "></i></span>
                <span>Dairy Free</span>
            </div>
            <div class="features-card">
                <span class="ketofriendly"><i class="fa-solid fa-bacon"></i></span>
                <span>Keto Friendly</span>
            </div>
        </div>
    </div>
    <!-- APP SECTION -->
    <div class="ordering-app-background">
        <div class="container">
            <div class="download-app">
                <span class="jumbotron-first-text">Download Our</span>
                <span class="jumbotron-second-text"><span>Ordering App</span></span>
                <div class="images-alignments">
                    <a href="#"><img src="../assets/img/app-store-badge.png" alt="app store"></a>
                    <a href="#"><img src="../assets/img/play-store-badge.png" alt="play store"></a>
                </div>
            </div>
        </div>
    </div>
    <!-- NEWS SECTION -->
    <div class="container">
        <div class="news-adjustments">
            <div class="main-subtitle">
                <h2>Latest News</h2>
            </div>
            <div class="button-container menu-button-adjustments">
                <a href="#"><span class="button">READ MORE NEWS <i class="fa-solid fa-circle-arrow-right"></i></span></a>
            </div>
        </div>
        <div class="news-cards">
            <div class="news-card">
                <img src="../assets/img/pancake-burger.jpg" alt="new pancake burger">
                <h2>NEW: The Pancake Burger</h2>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur, maxime magni odio corrupti obcaecati suscipit distinctio! Quasi dicta sint doloremque, ipsum vel aspernatur temporibus odit in nesciunt, laborum rerum. Provident!
            </div>
            <div class="news-card">
                <img src="../assets/img/new-milkshake-menu.jpg" alt="new milkshake menu">
                <h2>NEW: Milkshake Menu</h2>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Temporibus commodi ea ipsam aperiam molestiae eligendi architecto possimus, pariatur iusto magnam obcaecati repudiandae quae fugit distinctio adipisci eveniet iure tempore ullam!
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            categories:["APPETIZERS", "BURGERS", "PIZZAS", "FRIES", "SIDES", "DESSERTS", "BEVERAGES", "SPECIALS"],
            categoriesImages:[require("../assets/img/appetizers-menu-background.jpg"), require("../assets/img/burgers-menu-background.jpg"), require("../assets/img/pizza-menu-background.jpg"), require("../assets/img/fries-menu-background.jpg"), require("../assets/img/sides-menu-background.jpg"), require("../assets/img/desserts-menu-background.jpg"), require("../assets/img/beverages-menu-background.jpg"), require("../assets/img/specials-menu-background.jpg")],
            featuresIcons:[""]
        }
    },
    methods:{
        getImg(imgpath){
            return imgpath
        }
    }
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
    // MENU SECTION
    .menu-adjustments{
        padding-top: 150px;
        padding-bottom: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .menu-button-adjustments{
        padding: 0;
        margin: 0;
    }
    // ILLUSTRATIONS
    .menu-illustrations{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        row-gap: 1rem;
    }
    .card{
        height: calc(90% / 2);
        width: calc(90% / 4);
        position: relative;
    }
    .card span{
        color: white;
        font-weight: bold;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%);
    }
    // FEATURES CARD
    .features-illustrations{
        display: flex;
        justify-content: space-between;
        margin-top: 3rem;
    }
    .features-card{
        width: calc(90% / 4);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .vegetarian{
        color: green;
        font-size: 3rem;
        padding-bottom: 1rem;
    }
    .glutenfree{
        color: yellow;
        font-size: 3rem;
        padding-bottom: 1rem;
    }
    .dairyfree{
        color: lightblue;
        font-size: 3rem;
        padding-bottom: 1rem;
    }
    .ketofriendly{
        color: red;
        font-size: 3rem;
        padding-bottom: 1rem;
    }
    // ORDERING APP SECTION
    .ordering-app-background{
        background-image: url(../assets/img/app-ordering-scaled.jpg);
        background-size: cover;
        margin-top: 150px;
        padding-top: 150px;
    }
    .download-app{
        width: 50%;
        padding-bottom: 200px;
    }
    .download-app span{
        display: block;
    }
    .download-app img{
        width: 30%;
        margin-right: 1rem;
        margin-top: 2rem;
    }
    // NEWS SECTION
    .news-adjustments{
        padding-top: 150px;
        padding-bottom: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .news-cards{
        margin-bottom: 150px;
        display: flex;
        justify-content: space-between;
    }
    .news-card{
        width: calc(90% / 2);
        text-align: center;
    }
    .news-card h2{
        font-size: 2.3rem;
        margin: 1rem 0;
    }
</style>