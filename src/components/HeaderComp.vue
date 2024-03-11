<template>
    <header class="site-header">
        <!-- header navigation bar -->
        <div class="container">
            <div class="row pickwick-header">
                <div class="header-logo">
                    <div class="logo">
                        <a href="#" class="custom-logo-link">
                            <img class="custom-logo" src="/public/img/Logo.jpg" alt="Logo">
                        </a>
                    </div>
                </div>
                <div class="nav-with-sign-btn">
                    <nav class="main-navigation">
                        <div class="d-flex align-items-center h-100 justify-content-end">
                            <div class="menu-header-menu-container">
                                <ul class="menu">
                                    <li class="menu-item"><a href="#" v-for="navLink in navMenu" :key="navLink.id">{{ navLink.link }}</a></li>
                                </ul>
                            </div>
                            <!-- <button class="burger-menu">
                                <i class="fa-solid fa-bars"></i>
                            </button> -->
                            <div class="sign-up-in-container">
                                <div class="sign-in-btn">
                                    <span class="sign-in">Sign-In</span>
                                </div>
                            </div>
                        </div>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComp',
        data(){
            return {
                navMenu: [
                    {
                        link: 'Home'
                    },
                    {
                        link: 'About'
                    },
                    {
                        link: 'Academics'
                    },
                    {
                        link: 'Courses'
                    },
                    {
                        link: 'News'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;


    header{
        position: relative;
        display: flex;
        align-items: center;
        background: #ffffffd9;
        width: 100%;
        z-index: 9;
        min-height: 75px;
    }
    .site-header{
        content: "";
        display: table;
        table-layout: fixed;
    }
    .container{
        max-width: 1170px;
    }
    .pickwick-header{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .header-logo{
        width: 150px;
        order: -2;
    }
    .logo{
        position: absolute;
        z-index: 99;
        width: 100px;
        display: flex;
        align-items: center;
        height: 100%;
        top: 0;
    }
    li a{
        text-decoration: none;
    }
    li a:hover{
        color: $bg-red;
    }
    .costum-logo-link{
        display: inline-block;
    }
    a, a:after, a:before{
        transition: all 0.3s ease-in-out;
    }
    img{
        max-width: 100%;
        height: auto;
    }
    .nav-width-sign-btn{
        display: flex;
        align-items: center;
        justify-content: end;
    }
    .main-navigation{
        height: 75px;
    }
    .menu{
        margin: 0;
        padding: 0;
        list-style-position: inside;
    }
    .main-navigation li{
        display: inline-block;
        position: relative;
        list-style: none;
    }
    .main-navigation a{
        font-weight: 700;
        text-transform: capitalize;
        display: inline-block;
        position: relative;
        padding: 5px 0;
        font-size: 14px;
        margin-left: 35px;
        color: #192836;
    }
    .sign-up-in-container{
        margin-left: 30px;
        width: max-content;
        top: 20px;
        right: 20px;
        z-index: 1;
    }
    .sign-in-btn{
        height: inherit;
        display: flex;
        align-items: center;
        justify-content: end;
    }
    .sign-in{
        cursor: pointer;
        padding: 10px 18px 12px 18px;
        color: #34495e;
        text-decoration-color: #34495e;
        background-color: #ffffff;
        border-radius: 4px;
        box-shadow: 0px 2px 6px 0px rgb(196 196 196 / 57%);
        transition: all 0.2s;
        font-weight: 600;
        font-size: 14px;
        margin-top: -3px;
    }
    .sign-in:hover{
        background-color: $bg-red;
        color:$bg-light;
        transition-duration: 0.5s;
    }
    // .burger-menu{
    //     border: unset;
    //     background-color: unset; 
    // }
    // .burger-menu i{
    //     font-size: 35px;
    //     color: #34495e;
    // }
    // @media screen and (max-width: 666px){
    //     .menu-header-menu-container .menu{
    //         display: none;
    //     }
    // }
    

</style>