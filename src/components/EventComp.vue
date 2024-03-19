<template>
    <section class="d-flex align-items-center justify-content-center mt-5">
        <div class="container d-flex align-items-center justify-content-center">
               <div class="left">
                    <img src="/public/img/video-bg-3.jpg" alt="">
                </div>
                <div class="right d-flex justify-content-center">
                    <div class="content">
                        <h2 class="text-center p-3">Upcoming Events</h2>
                        <div>
                            <img src="" alt="">
                            <p>Princeton offers admission information sessions and student-led tours to campus visitors</p>
                            <span><strong>Learn more</strong></span>
                        </div>
                        <div>
                            <img src="" alt="">
                            <p>Admission information sessions and student-led tours to campus visitors</p>
                            <span><strong>Learn more</strong></span>
                        </div>
                    </div>
                </div> 
        </div>
    </section>
</template>

<script>
    export default {
        name: 'EventComp',
        data() {
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    
    .left{
        width: 50%;
        height: 500px;
        border-radius: 10px;
    }
    .left img{
        width: 100%;
        height: 100%;
        border-radius: 10px;
    }
    .right{
        width: 50%;
        min-height: 500px;
        border-radius: 10px;
        margin-left: -200px;
        margin-bottom: -150px;
        border: 1px solid;
        background-color: white;
        padding: 0 30px 50px;
        z-index: 9;
    }
    div h2{
        color: white;
        background-color: $bg-red;
    }
    .content div{
        padding-top: 30px;
    }
    .content p{
        font-size: 20px;
    }
    @media screen and (max-width: 767px){
        .left, .right{
            width: 100%;
        }
        .left{
            height: 400px;
        }
        .left img{
            height: 80%;
        }
        .right{
            min-height: 400px;
        }
    }
</style>