<template>

  <HeaderComp />
  <HeroComp />
  <MainComp />

  <div class="main-carousel border">
    carousel
  </div>

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
      FooterComp
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