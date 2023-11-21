<template>
    <header>
        <!-- header navigation bar -->
        <nav class="container d-flex justify-content-between align-items-center ">
            <img class="logo" src="/public/img/Logo.jpg" alt="Logo">
            <ul class="d-flex">
                <li class="m-2" v-for="navLink in navMenu" :key="navLink.id"><a href="#">{{ navLink.link }}</a></li>
            </ul>
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
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .logo{
        width: 100px;
    }
    li{
        list-style: none;
    }
    a{
        color: $bg-lightblack;
        text-decoration: none;
    }


</style>