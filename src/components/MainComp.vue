<template>
    <main>
        <PartnerComp/>
        <CourseComp/>
        <EventComp/>
    </main>
</template>

<script>
import PartnerComp from './PartnerComp.vue';
import CourseComp from './CourseComp.vue';
import EventComp from './EventComp.vue';
    export default {
        name: 'MainComp',
        components:{
            PartnerComp,
            CourseComp,
            EventComp,
        }
    }
</script>

<style lang="scss" scoped>

</style>