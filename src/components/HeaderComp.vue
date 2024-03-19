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
                        <!-- <li class="nav-item border mx-2">
                            <a class="nav-link" href="#">Login</a>
                        </li>
                        <li class="nav-item border">
                            <a class="nav-link" href="#">Register</a>
                        </li> -->
                    </ul>
                </div>
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
        border: $bg-red;
    }
</style>