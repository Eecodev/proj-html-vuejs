<template>
  <!-- <meta name="viewport" content="width=device-width, initial-scale=1.0"> -->
  <HeaderComp/>
  <HeroComp/>
  <MainComp/>
  <FooterComp/>
  
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import HeroComp from './components/HeroComp.vue'
import MainComp from './components/MainComp.vue'
import FooterComp from './components/FooterComp.vue'
  export default {
    name: 'App',
    components: {
      HeaderComp,
      HeroComp,
      MainComp,
      FooterComp,
    },
    data(){
      return {

      }
    },
    methods: {

    }
  }
</script>

<style lang="scss" scoped>

</style>