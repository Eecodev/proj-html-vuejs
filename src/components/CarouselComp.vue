<template>


        <div class="d-flex">
            <div class="main-carousel" v-for="slide in slides" :key="slide.id">
                <img :src="slide.img" alt="slide">
            </div>
        </div>  
    
</template>

<script>
    export default {
        name: 'CarouselComp',
        data() {
            return {
                slides: [
                    {
                        img: '/public/img/gallery-1-3(1).jpg'
                    },
                    {
                        img: '/public/img/gallery-2-3(1).jpg'
                    },
                    {
                        img: '/public/img/gallery-3-3(1).jpg'
                    },
                    {
                        img: '/public/img/gallery-2-3.jpg'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>

    img{
        width: 100%;
    }
    .main-carousel{
        display: inline-block;
        overflow: hidden;
        
    }
    img:hover{
        transform: scale(1.5);
        transition: .5s ease-in-out;
    }
</style>