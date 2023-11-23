<template>
    <main>
        <PartnerComp/>
        <CourseComp/>
    </main>
</template>

<script>
import PartnerComp from './PartnerComp.vue';
import CourseComp from './CourseComp.vue';
    export default {
        name: 'MainComp',
        components:{
            PartnerComp,
            CourseComp,
        }
    }
</script>

<style lang="scss" scoped>

</style>