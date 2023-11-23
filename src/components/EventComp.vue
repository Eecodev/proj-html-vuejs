<template>
    <main>
        <section id="event" class="container">

               <div class="quote-container">
                    <img class="quote-img" src="/public/img/quote.png" alt="quote">
                    <h4 class="quote-text">
                        "Academics was committed to my success from the moment I attended an Open House. With the support of caring <span class="red-text">advisors, professors, and staff</span> i was able to thrive in courses, gain recognition through scholarships, and finish with confidence in my <span class="red-text">@academics</span> abilities."</h4>
                </div> 
            
                <div class="content-container d-flex mt-5">
                    <img class="video-img" src="/public/img/video-bg-3.jpg" alt="">
                    <div class="events-container">
                        <h3 class="text-center">Upcoming Events</h3>
                        <h5>Princeton offers admision information sessions an student-led tours to campus visitors</h5>
                        <p><small>Learn more</small></p>
                        <h5>Admission information sessions and student-led tours to campus visitors</h5>
                        <p><small>Learn more</small></p>
                        <p class="text-center"><small>Event Locations</small></p>
                    </div> 
                </div>
                
        </section>
    </main>
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

    .red-text{
        color: $bg-red;
    }
    .quote-container {
        position: relative;
        text-align: center;
        padding-top: 40px;

    }

    .quote-img {
        width: 160px;
        display: block;
        margin: 0 auto; 
    }

    .quote-text {
        position: absolute;
        padding: inherit;
        top: 50%; 
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
        max-width: 80%;
        font-size: 18px; 
        line-height: 1.5; 
    }

    .content-container{
        position: relative;
    }
    .video-img{
        width: 500px;
        display: block;
        margin: 0 auto;
    }
    .events-container{
        width: 500px;
        position: absolute;
        top: 50px;
        right: 100px;
        background-color: $bg-light;
        padding: 40px 20px 50px 30px;
    }

    
</style>