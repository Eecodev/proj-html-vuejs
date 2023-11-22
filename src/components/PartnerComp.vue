<template>
    <main>
        <section id="partnership" class="container m-5">
            <h3>Since 2000, we've been partnering with education leaders to <span class="red-text">increase equity and achievement</span> for all students</h3>

            <div class="d-flex justify-content-center align-items-center">
                <div v-for="card in cardPartner" :key="card.id" class="card text-center m-2" style="width: 18rem;">
                    <div class="card-body">
                        <img class="card-img" :src="card.img" :alt="card.title">
                        <h5 class="card-title mb-2">{{ card.title }}</h5>
                        <p class="card-text mb-2">{{ card.text }}</p>
                    </div>
                </div>
            </div>

            <div class="d-flex justify-content-center mt-4">
                <div class="d-flex align-items-center m-4" v-for="statistic in statistics" :key="statistic.id" :style="{ backgroundImage: 'ulr(' + statistic.img +')'}">
                    <h2>{{ statistic.value }}</h2>
                    <p>{{ statistic.label }}</p>
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
                statistics: [
                    {
                        id: 1,
                        value: '6500 +',
                        label: 'Students',
                        img: '/public/img/counter-shape-1-1-1.png'
                    },
                    {
                        id: 2,
                        value: '200 +',
                        label: 'Online Courses',
                        img: '/public/img/counter-shape-2-1-1.png'
                    },
                    {
                        id: 3,
                        value: '100% +',
                        label: 'Happy Clients',
                        img: '/public/img/counter-shape-3-1-1.png'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    h3{
        text-align: center;
        padding-bottom: 40px;
    }
    .red-text{
        color: $bg-red;
    }
    .card-img{
        width: 60px;
        margin-bottom: 20px;
    }
</style>