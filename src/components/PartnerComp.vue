<template>
    <main>
        <section id="partnership" class="m-3 m-md-5">
            <div class="container title-partner-container">
               <h2>Since 2000, we've been partnering with education leaders to <br><span class="red-text">increase equity and achievement</span> for all students</h2> 
            </div>
            

            <div class="container">
                <div class="row justify-content-center">
                    <div v-for="card in cardPartner" :key="card.id" class="col-xs-2 col-sm-6 col-md-4 col-lg-3 mb-3">
                        <div class="card text-center border-shadow">
                            <div class="card-body p-4">
                                <img class="card-img" :src="card.img" :alt="card.title">
                                <h5 class="card-title mt-3 mb-2">{{ card.title }}</h5>
                                <p class="card-text">{{ card.text }}</p>
                            </div>
                        </div>
                    </div> 
                </div>
            </div>

            <div class="container mt-5">
                <div class="row justify-content-center">
                    <div class="col-sm-6 col-md-4 col-lg-3 mb-3 align-items-center ">
                        <div class="statistics d-flex">
                            <h2 class="mx-2">
                                <span class="stat-orange">6500 +</span>
                                <strong>Students</strong>
                            </h2>
                            <img src="/public/img/counter-shape-1-1-1.png" alt="">
                        </div>
                    </div>
                    <div class="col-sm-6 col-md-4 col-lg-3 mb-3">
                        <div class="statistics d-flex">
                            <h2 class="mx-2">
                                <span class="stat-red">200 +</span>
                                <strong>Online Courses</strong>
                            </h2>
                            <img src="/public/img/counter-shape-2-1-1.png" alt="">
                        </div>
                    </div>
                    <div class="col-sm-6 col-md-4 col-lg-3 mb-3">
                        <div class="statistics d-flex">
                            <h2 class="mx-2">
                                <span class="stat-green">100%</span>
                                <strong>Happy Clients</strong>
                            </h2>
                            <img src="/public/img/counter-shape-3-1-1.png" alt="">
                        </div>
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
                // statistics: [
                //     {
                //         id: 1,
                //         value: '6500',
                //         label: 'Students',
                //     },
                //     {
                //         id: 2,
                //         value: '200',
                //         label: 'Online Courses',
                //     },
                //     {
                //         id: 3,
                //         value: '100%',
                //         label: 'Happy Clients',
                //     }
                // ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;


    #partnership{
        text-align: center;
    }
    .title-partner-container{
        margin: 70px 0;
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
    .statistics h2, .vertical-align {
        margin: 0; 
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

    @media screen and (max-width: 575px){
        .statistics{
            flex-direction: column;
            justify-content: center;
        }
        .statistics img{
            position: absolute;
            left: 35%;
            right: 65%;
        }
    }
</style>