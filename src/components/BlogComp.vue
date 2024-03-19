<template>
    <main>
        <section id="blog">
            <div class=" container blog-latest">
                <h3 class="pb-3">Latest From Our Blogs</h3>
                <p class="pb-4">Whether you're considering a foundation course or an undergraduate degree master's <br> or a PhD, academics is a place where students thrive</p>
            </div>

            <div class="container">
                <div class="row d-flex justify-content-center mb-5">
                   <div class="card m-2 p-0" style="width: 18rem;" v-for="blog in posts" :key="blog.id">
                        <div class="col">
                           <div class="card-body p-0">
                                <img :src="blog.img" class="card-img-top" :alt="blog.about">  
                                <div class="d-flex px-2 pt-2">
                                    <p class="card-text"><small class="text-body-secondary">{{ blog.admin }}</small></p>
                                    <p class="card-text px-2"><small class="text-body-secondary">{{ blog.edu }}</small></p>  
                                </div>
                                
                                <h5 class="card-title px-2">{{ blog.about }}</h5>
                                <p class="card-text px-2"><small class="text-body-secondary"><span>{{ blog.read }}</span></small></p>
                            </div> 
                        </div>
                    </div> 
                </div>
            </div>

            <!-- <div class="container">
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
            </div> -->
        </section>
    </main>
</template>

<script>
    export default {
        name: 'BlogComp',
        data() {
            return {
                posts: [
                    {
                        img: '/public/img/news-3-2.jpg',
                        admin: 'Admin',
                        edu: 'University',
                        about: 'Peer pressure changes how teens tackle inequality',
                        read: 'Read more'
                    },
                    {
                        img: '/public/img/news-2-2.jpg',
                        admin: 'Admin',
                        edu: 'Education',
                        about: 'Lewisham Live Mixtape celebrates boroughs',
                        read: 'Read more'
                    },
                    {
                        img: '/public/img/news-1-2.jpg',
                        admin: 'Admin',
                        edu: 'University',
                        about: 'Turner Prize winners work to open Gold on film festival',
                        read: 'Read more'
                    }
                ]
            }
        }

    }
</script>

<style lang="scss" scoped>
    .blog-latest{
        text-align: center;
        margin-top: 150px;
    }
    h5{
        font-size: 20px;
    }
</style>