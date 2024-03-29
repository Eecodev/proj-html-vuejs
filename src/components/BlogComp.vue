<template>
    <main>
        <section id="blog">
            <div class=" container blog-latest">
                <h3 class="pb-3 fs-1">Latest From Our Blogs</h3>
                <p class="pb-4 fs-4">Whether you're considering a foundation course or an undergraduate degree master's <br> or a PhD, academics is a place where students thrive</p>
            </div>

            <div class="container">
                <div class="row d-flex justify-content-center mb-5">
                   <div class="card m-3 p-0 border-shadow" style="width: 350px;" v-for="blog in posts" :key="blog.id">
                        <div class="col">
                           <div class="card-body p-0">
                                <img :src="blog.img" class="card-img-top" :alt="blog.about">  
                                <div class="p-2">
                                    <div class="d-flex px-2 pt-2">
                                        <p class="card-text f-admin"><i class="fa-regular fa-user"></i><small class="text-body-secondary">{{ blog.admin }}</small></p>
                                        <p class="card-text px-4 f-admin"><i class="fa-regular fa-folder"></i><small class="text-body-secondary">{{ blog.edu }}</small></p>  
                                    </div>
                                
                                    <p class="card-title px-2 lh-lg fs-5"><strong>{{ blog.about }}</strong></p>
                                    <hr>
                                    <p class="card-text px-2"><small class="text-body-secondary"><span>{{ blog.read }}</span></small></p> 
                                </div>
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
@use '../assets/styles/partials/variables' as *;
    .border-shadow{
        box-shadow: 0px 28px 65px 0px rgba(188, 188, 188, 0.25);
    }
    .blog-latest{
        text-align: center;
        margin-top: 200px;
    }
    h5{
        font-size: 20px;
    }
    .f-admin:hover{
        color: $bg-red;
    }
    // icons
    .fa-user, .fa-folder{
        padding-right: 15px;
    }

</style>