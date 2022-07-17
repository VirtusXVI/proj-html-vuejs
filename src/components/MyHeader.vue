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
            <section>
                <div class="jumbotron-container">
                    <div>
                        <span>Hungry?</span>
                    </div>
                    <div>
                        <span>Great Food Delivered</span>
                    </div>
                    <div>
                        <span><a href="#">Button</a></span>
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
        background-size: contain;
        background-repeat: no-repeat;
    }
    .header-container{
        width: 60%;
        margin: 0 auto;
    }
    .header-content{
        padding-top: 2rem;
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
        color: yellow;
    }
    // JUMBOTRON
    .jumbotron-container{
        width: 30%;
    }
</style>