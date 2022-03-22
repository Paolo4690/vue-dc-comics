<template>
  <div id="app">
    <HeaderComics/>
    <MainComics/>
    <FooterComics/>
  </div>
</template>

<script>
import HeaderComics from './components/HeaderComics.vue'
import MainComics from './components/MainComics.vue'
import FooterComics from './components/FooterComics.vue'

export default {
  name: 'App',
  components: {
    HeaderComics,
    MainComics,
    FooterComics
  }
}
</script>

<style lang="scss">
@import './assets/styles/style';

</style>
