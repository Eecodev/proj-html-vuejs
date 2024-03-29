<template>
    <header>
        <!-- header navigation bar -->
        <nav class="navbar navbar-expand-md navbar-light bg-white shadow-sm p-0">
            <div class="container">
                <a class="navbar-brand d-flex align-items-center p-0" href=“#”>
                    
                        <img class="header-logo" src="/img/Logo.jpg" alt="Logo">
                    
                </a>

                <button class="navbar-toggler" type="button" @click="toggleMenu()" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>

                <div class="navbar-collapse collapse" :class="{'show': showMenu}" id="navbarSupportedContent">

                    <!-- Right Side Of Navbar -->

                    
                    <ul class="navbar-nav ms-auto">
                        <li v-for="(item, index) in navMenu" :key="index" class="nav-item">
                            <a class="nav-link" href="#">{{ item.link }}</a>
                        </li>
                    </ul>
                </div>
                <!-- <button class="btn btn-danger">Sign-In</button> -->
            </div>
        </nav>
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
                ],
                showMenu: false
            }
        },
        methods:{
            toggleMenu(){
                this.showMenu = !this.showMenu;
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

    .header-logo{
        width: 100px;
    }
    li a{
        text-decoration: none;
        margin: 8px;
    }
    li a:hover{
        padding-bottom: 5px;
        border-bottom: 2px solid $bg-red;
    }
    @media screen and (max-width: 767px){
        .nav-link{
            margin-left: 0;
            padding: 10px;
            border-radius: 15px;
        }
        li a:hover{
            background-color: $bg-red;
            color: $bg-light;
            border: 2px solid;
            text-decoration: none;
        }
    }
</style>