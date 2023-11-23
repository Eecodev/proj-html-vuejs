<template>
    <main>
        <PartnerComp/>
        <CourseComp/>
        <EventComp/>
        <BlogComp/>
        <CarouselComp/>
    </main>
</template>

<script>
import PartnerComp from './PartnerComp.vue';
import CourseComp from './CourseComp.vue';
import EventComp from './EventComp.vue';
import BlogComp from './BlogComp.vue';
import CarouselComp from './CarouselComp.vue';
    export default {
        name: 'MainComp',
        components:{
            PartnerComp,
            CourseComp,
            EventComp,
            BlogComp,
            CarouselComp
        }
    }
</script>

<style lang="scss" scoped>

</style>