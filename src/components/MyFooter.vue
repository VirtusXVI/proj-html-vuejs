<template>
  <div class="footer-background">
    <div class="footer-container">
        <div class="footer-nav-adjustments">
            <div class="footer-nav">
                <h4>ORDER ONLINE</h4>
                <div v-for="element in onlineOrder" :key="element">
                    <a href="#">{{ element }}</a>
                </div>
            </div>
            <div class="footer-nav">
                <h4>NAVIGATE</h4>
                <div v-for="element in footerNavbarOptions" :key="element" v-html="element">
                </div>
            </div>
            <div class="footer-nav">
                <h4>INFORMATION</h4>
                <div v-for="element in generalInfo" :key="element">
                    <a href="#">{{ element }}</a>
                </div>
                <div>
                    <a href="#"><img src="../assets/img/app-store-badge-200x67.png" alt="app store"></a>
                    <a href="#"><img src="../assets/img/play-store-badge-200x67.png" alt="app store"></a>
                </div>
            </div>
            <div class="footer-nav">
                <h4>OPENING HOURS</h4>
                <div v-for="element in openingHours" :key="element" v-html="element">
                </div>
            </div>
            <div class="footer-nav">
                <section class="coupon-adjustments">
                    <h4>VOUCHER</h4>
                    <img src="../assets/img/footer-coupon.png" alt="">
                    <span>Just Use The Code</span>
                    <span class="highlighted bigger">FIRSTORDER</span>
                    <span>At Checkout</span>
                </section>
            </div>
        </div>
    </div>
    <div class="lower-footer-container">
        <div>
            <img class="footer-logo" src="../assets/img/takeout-logo.png" alt="logo">
        </div>
        <div>
            <span class="lower-footer-subtitle">Stay In The Loop</span>
            <span>Sign up to receive up to date news and offers direcly in your inbox:</span>
        </div>
        <form>
            <div>
                <label for="Email"></label>
                <input class="form-text" type="Email" id="Email" placeholder="youremail@gmail.com">
            </div>
            <button class="form-button" type="submit">SUBSCRIBE</button>
        </form>
        <div class="socials">
            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
            <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="#"><i class="fa-brands fa-youtube"></i></a>
            <a href="#"><i class="fa-regular fa-envelope"></i></a>
        </div>
    </div>
  </div>
</template>

<script>
    export default {
        props:{
            footerNavbarOptions: Array,
            onlineOrder: Array,
            generalInfo: Array,
            openingHours: Array
        }
    }
</script>

<style lang="scss" scoped>
    @import "../assets/scss/common.scss";
    // COMMON
    a{
        color: white;
    }
    // FOOTER
    .footer-background{
        background-image: url(../assets/img/footer-background-scaled.jpg);
        background-size: cover;
        background-repeat: no-repeat;
    }
    .footer-container{
        width: 80%;
        margin: 0 auto;
    }
    .footer-nav-adjustments{
        margin-top: 150px;
        padding-top: 100px;
        display: flex;
        justify-content: space-between;
        color: white;
    }
    .footer-nav{
        width: calc(90% / 5);
        font-weight: bold;
    }
    .footer-nav h4{
        padding-bottom: 1rem;
    }
    .footer-nav div{
        margin-top: 1rem;
    }
    .footer-nav img{
        width: 50%;
        display: block;
        margin-top: 1rem;
    }
    .footer-nav a img{
        border: 2px solid white;
        border-radius: 10px;
    }
    .coupon-adjustments{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .coupon-adjustments img{
        width: 70%;
        margin-bottom: 0.5rem;
    }
    .bigger{
        font-size: 1.5rem;
    }
    // LOWER FOOTER
    .lower-footer-container{
        width: 30%;
        margin: 0 auto;
        text-align: center;
        color: white;
        padding-top: 100px;
    }
    .lower-footer-container *{
        margin-bottom: 2rem;
    }
    .lower-footer-container span{
        display: block;
    }
    .footer-logo{
        width: 200px;
    }
    .lower-footer-subtitle{
        font-size: 3rem;
        color: #fcd66c;
        font-weight: bold;
    }
    .form-text{
        width: 100%;
        padding: 0.8rem 0;
        border-radius: 25px;
        text-align: center;
    }
    .form-button{
        width: 100%;
        padding: 0.8rem 0;
        border-radius: 25px;
        background-color: #cc1a26;
        color: white;
        font-weight: bold;
    }
    .socials{
        width: 30%;
        margin: auto;
        display: flex;
        justify-content: space-between;
        padding-bottom: 420px;
    }
</style>