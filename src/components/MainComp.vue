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
    export default {
        name: 'MainComp',
        components:{
            PartnerComp,
            CourseComp,
            EventComp,
            BlogComp,
        }
    }
</script>

<style lang="scss" scoped>

</style>