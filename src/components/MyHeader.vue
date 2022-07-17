<template>
    <div class="header-background">
        <div class="header-container">
            <!-- LOGO + NAV SECTION -->
            <section class="header-content">
                <!-- LOGO -->
                <div>
                    <img src="../assets/img/takeout-logo.png" alt="logo">
                </div>
                <!-- NAVBAR -->
                <nav>
                    <ul class="navbar">
                        <li @click="setActiveMenuVoice(index)" v-for="option,index in navbarOptions"  :key="index"><a :class="activeMenuVoice === index ? 'active' : ''" href="#" v-html="option"></a></li>
                    </ul>
                </nav>
            </section>
            <!-- JUMBOTRON SECTION -->
            <section class="jumbotron-adjustments">
                <div class="jumbotron-container">
                    <div>
                        <span class="jumbotron-first-text">Hungry?</span>
                    </div>
                    <div>
                        <span class="jumbotron-second-text"><span>Great Food</span> Delivered</span>
                    </div>
                    <div class="button-container">
                        <a href="#"><span class="jumbotron-button">VIEW OUR MENU <i class="fa-solid fa-circle-arrow-right"></i> </span></a>
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                navbarOptions:['Home <i class="fa-solid fa-chevron-down"></i>', "Order Online", "About", "News", "Contact Us", '<i class="fa-solid fa-cart-shopping"></i>'],
                activeMenuVoice: 0,
            }
        },
        methods:{
            // FUNCTION THAT SETS ACTIVE NAV ELEMENT
            // ToDo:prevent page reload when clicking a nav element
            setActiveMenuVoice(index){
                this.activeMenuVoice = index;
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "../assets/scss/common.scss";
    .header-background{
        background-image: url(../assets/img/home-background-hero-scaled.jpg);
        background-size: cover;
        background-repeat: no-repeat;
    }
    .header-container{
        width: 60%;
        margin: 0 auto;
    }
    .header-content{
        padding-top: 100px;
        display: flex;
        justify-content: space-between;
    }
    // LOGO
    .header-content div{
        width: 30%;
    }
    // NAVBAR
    nav{
        display: flex;
        align-items: center;
        width: 50%;
    }
    .navbar{
        display: flex;
        justify-content: space-between;
        width: 100%;
    }
    // ACTIVE CLASS
    .active{
        color: $color-cube-9;
    }
    // JUMBOTRON
    .jumbotron-adjustments{
        padding-top: 250px;
    }
    .jumbotron-container{
        width: 40%;
    }
    .jumbotron-first-text{
        font-size: 2.5rem;
        color: $color-cube-1;
        font-weight: bold;
    }
    .jumbotron-second-text{
        font-size: 5rem;
        color: $color-cube-1;
        font-weight: bold;
    }
    .jumbotron-second-text span{
        color: $color-cube-9;
    }
    // BUTTON
    .button-container{
        margin-top: 2rem;
        padding-bottom: 400px;
    }
    .jumbotron-button{
        padding: 0.8rem 2rem;
        background-color: $color-cube-3;
        border-radius: 25px;
        color: $color-cube-1;
        font-weight: bold;
    }
</style>