<template>
    <div class="elementor">
       <div class="twitet">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <p class="quote-text">"Academics was committed to my success from the moment I attended an Open <br> House. With the support of caring <a href="#">advisors, professors, and staff</a> i was able to <br>thrive in courses, gain recognition through scholarships, and finish <strong>with <br>confidence in my</strong> <a href="#">@academics</a> <strong>abilities."</strong></p>
                    </div>
                </div>
            </div>
        </div> 
    </div>
    
        
        <section id="event" class="d-flex container">
            <div class="position-relative d-flex justify-content-center align-items-center flex-grow-1">
                <div class="content-container mt-5">
                    <img class="video-img" src="/public/img/video-bg-3.jpg" alt="">
                </div>
                <div class="events-container">
                    <div class="border">
                        <h3 class="text-center">Upcoming Events</h3>  
                    </div>
                    <h5 class="mt-5 ms-2">Princeton offers admission information sessions an student-led tours to campus visitors</h5>
                    <p class="m-2"><small>Learn more</small></p>
                    <h5 class="mt-4 m-2">Admission information sessions and student-led tours to campus visitors</h5>
                    <p class="m-2"><small>Learn more</small></p>
                    <p class="text-center mt-5"><small>Event Locations</small></p>
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
    .twitet {
        color: #192836;
        font-size: 30px;
        text-align: center;
    }
    .twitet p {
        margin-bottom: 30px;
        position: relative;
        z-index: 1;
        margin-top: 60px;
        overflow: hidden;
    }

    .twitet a{
        font-size: 30px;
        color: #d74d52;
        font-weight: 700;
        position: relative;
        display: inline-block;
        word-break: break-all;
        text-decoration: none;
    }
    a, a:after, a:before {
        color: #192836;
        transition: all 0.4s ease-in-out;
    }

    .twitet p a:after {
        content: "";
        background: #d74d52;
        height: 1px;
        width: 100%;
        right: 0;
        bottom: 0;
        position: absolute;
        margin-left: 5px;
        transition: all 0.4s ease-in-out;
    }
    .position-relative{
        position: relative;
    }
    .video-img{
        max-width: 100%;
        height: auto;
        display: block;
        margin: 0 auto;
    }
    .events-container{
        max-width: 100%; 
        height: auto;
        position: absolute;
        bottom: -50px; 
        right: 10%; 
        background-color: $bg-light;
        padding: 0 20px 0px 30px;
    }

    
</style>