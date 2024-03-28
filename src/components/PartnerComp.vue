<template>
    <main>
        <section id="partnership" class="m-3 m-md-5">
            <div class="container">
               <h2>Since 2000, we've been partnering with education leaders to <br><span class="red-text">increase equity and achievement</span> for all students</h2> 
            </div>
            

            <div class="container">
                <div class="row justify-content-center">
                    <div v-for="card in cardPartner" :key="card.id" class="col-xs-2 col-sm-6 col-md-4 col-lg-3 p-3 my-card">
                        <div class="card text-center border-shadow">
                            <div class="card-body py-5">
                                <img class="card-img" :src="card.img" :alt="card.title">
                                <h5 class="card-title mt-3 mb-4">{{ card.title }}</h5>
                                <p class="card-text lh-lg">{{ card.text }}</p>
                            </div>
                        </div>
                    </div> 
                </div>
            </div>

            <div class="container mt-5">
                <div class="row justify-content-center mb-5">
                    <div class="col-sm-6 col-md-4 col-lg-3 mb-3">
                        <div class="statistics">
                            <h2 class="d-flex justify-content-start align-items-center">
                                <span class="stat-orange fw-bold">6500<span class="px-2">+</span></span>
                                <span class="fs-6">Students</span>
                            </h2>
                        </div>
                        <!-- <img src="/public/img/counter-shape-1-1-1.png" alt=""> -->
                    </div>
                    <div class="col-sm-6 col-md-4 col-lg-3 mb-3">
                        <div class="statistics">
                            <h2 class="d-flex justify-content-center align-items-center">
                                <span class="stat-red fw-bold">200<span class="px-2">+</span></span>
                                <span class="fs-6">Online Courses</span>
                            </h2>
                        </div>
                        <!-- <img src="/public/img/counter-shape-2-1-1.png" alt=""> -->
                    </div>
                    <div class="col-sm-6 col-md-4 col-lg-3 mb-3">
                        <div class="statistics">
                            <h2 class="d-flex justify-content-end align-items-center">
                                <span class="stat-green fw-bold">100<span class="px-2">%</span></span>
                                <span class="fs-6">Happy Clients</span>
                            </h2>
                        </div>
                        <!-- <img src="/public/img/counter-shape-3-1-1.png" alt=""> -->
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
    export default {
        name: 'PartnerComp',
        data(){
            return{
                cardPartner: [
                    {
                        img: '/public/svg/svg-0.svg',
                        title: 'Online Coaching',
                        text: 'Lorem ipsum is simply dummy text of the print ing and typesetting has been the industrys'
                    },
                    {
                        img: '/public/svg/svg-1.svg',
                        title: 'Consultation',
                        text: 'Lorem ipsum is simply dummy text of the print ing and typesetting has been the industrys'
                    },
                    {
                        img: '/public/svg/svg-2.svg',
                        title: 'Life Programs',
                        text: 'Lorem ipsum is simply dummy text of the print ing and typesetting has been the industrys'
                    },
                ],
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;


    #partnership{
        text-align: center;
    }
    h2{
        text-align: center;
        padding-bottom: 40px;
        font-size: 30px;
        line-height: 1.8em;
    }
    .red-text{
        color: $bg-red;
    }
    .my-card{
        width: 400px;
    }
    .border-shadow{
        box-shadow: 0px 28px 65px 0px rgba(188, 188, 188, 0.25);
    }
    .card-img{
        width: 60px;
        margin-bottom: 35px;
    }
    .statistics {
        position: relative;
        background-size: cover;
    }
    .statistics h2{
        font-size: 40px;
        padding: 0 30px;
        line-height: 1.2;
    }
    .statistics h2 strong{
        font-size: 15px;
        position: absolute;
        top: 14px;
        margin-left: 18px;
    }
    .statistics img{
        position: absolute;
        top: -8px;
        left: 40px;
        height: auto;
        max-width: 100%;
    }
    .stat-orange{
        color: #ef8b35;
    }
    .stat-red{
        color: #e15d63;
    }
    .stat-green{
        color: #72df7c;
    }

    @media screen and (max-width: 767px){

    }
    @media screen and (max-width: 575px){
        .statistics{
            justify-content: center;
            padding: 0;
        }
        .statistics img{
            position: absolute;
            left: 40%;
            right: 70%;
        }
    }
</style>