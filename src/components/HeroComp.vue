<template>
    <div id="hero">
        <div class="container hero-content">
            <h1>Professional Development <br>For Coaches And Leaders</h1>
            <a href="#" class="btn">Learn More</a>
        </div> 
    </div>
</template>

<script>
    export default {
        name: 'HeroComp'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    #hero{
        position: relative;
        height: 100vh;
        background-image: url('/public/img/jumbotron_1.PNG');
        background-size: cover;
        background-position: center;
        color: $bg-light;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .hero-content{
        max-width: 100%;
        margin: 0 auto;
    }
    .hero-content h1{
        font-weight: 10;
        font-size: 2.5rem;
        line-height: 1.5em;
        margin-bottom: 20px;
        color: $bg-lightblack;
    }
    .btn{
        display: inline-block;
        padding: 10px 20px;
        background-color: $bg-light;
        color: $bg-red;
        text-decoration: none;
        border-radius: 5px;
        border: 1px solid $bg-red;
        transition: background-color 0.3s ease;
    }
    .btn:hover{
        background-color: $bg-red;
        color:$bg-light;
    }

</style>