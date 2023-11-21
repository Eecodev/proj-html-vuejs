<template>
    <div id="hero">
        <div class="hero-content">
            <h1>Professional Development For Coaches And Leaders</h1>
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
    #hero{
        position: relative;
        height: 100vh;
        background-image: url('/public/img/jumbotron_1.PNG');
        background-size: cover;
        background-position: center;
        color: #fff;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .hero-content{
        max-width: 600px;
        margin: 0 auto;
    }
    .hero-content h1{
        font-size: 3rem;
        margin-bottom: 20px;
    }
    .btn{
        display: inline-block;
        padding: 10px 20px;
        background-color: #fff;
        color: #ff5500;
        text-decoration: none;
        border-radius: 5px;
        border: 1px solid #ff5500;
        transition: background-color 0.3s ease;
    }
    .btn:hover{
        background-color: #dd4400;
        color:#fff
    }

</style>