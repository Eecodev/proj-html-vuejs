<template>
    <main>
        <section id="course" class="mt-3">
            <div class="container text-center">
                <h3 class="mb-4">Recent Courses</h3>
                <p class="mb-5">Whether you're considering a foundation course or an undergraduate degree master's <br> or PhD, academics is a place where students thrive.</p>  
            </div>
            
            <div class="container">
                <div class="row justify-content-center">
                   <div class="card m-2 p-0" style="width: 18rem;" v-for="card in courseCard" :key="card.id">
                        <div class="col">
                            <div class="card-body p-0">
                                <img :src="card.img" class="card-img-top" :alt="card.about"> 
                                <p class="card-text p-2"><small class="text-body-secondary">{{ card.price }}</small></p>
                                <h5 class="card-title p-2">{{ card.about }}</h5>
                                <p class="card-text p-2">{{ card.description }}</p>
                                <p class="card-text p-2"><small class="text-body-secondary"><span class="red-text">{{ card.course_by }}</span></small></p>
                            </div>
                        </div>
                    </div> 
                </div>
            </div>
        </section>
    </main>
</template>

<script>
    export default {
        name: 'CourseComp',
        data() {
            return {
                courseCard: [
                    {
                        img: '/public/img/bruce-mars-FWVMhUa_wbY-unsplash.jpg',
                        price: 'Free',
                        about: 'UI Animation using Sketch 3, Principle App, and Flinto',
                        description: 'This online photography course will teach you how to take amazing images and even sell...',
                        course_by: 'Course by: University'
                    },
                    {
                        img: '/public/img/markus-spiske-N8yoH-dj4k8-unsplash.jpeg',
                        price: 'Free',
                        about: 'The Ultimate Drawing Course - Beginner to Advanced',
                        description: 'This online photography course will teach you how to take amazing images and even sell...',
                        course_by: 'Course by: University'
                    },
                    {
                        img: '/public/img/william-thomas-ny6tO4ItOEY-unsplash.jpg',
                        price: 'Free',
                        about: 'Your Complete Guide to Photography',
                        description: 'This online photography course will teach you how to take amazing images and even sell...',
                        course_by: 'Course by: University'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .text-center{
        text-align: center;
    }

    .red-text{
        color: $bg-red;
    }
    // .zoom-img{
    //     display: inline-block;
    //     overflow: hidden;
    // }
</style>