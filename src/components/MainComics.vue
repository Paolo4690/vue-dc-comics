<template>
  <main>
    <JumboMain />
    <TopMain />
    <EndMain />
  </main>
</template>

<script>
import JumboMain from './JumboMain.vue'
import TopMain from './TopMain.vue'
import EndMain from './EndMain.vue'

export default {
  name: 'MainComics',
  components: {
    JumboMain,
    TopMain,
    EndMain
  }
}
</script>

<style>

</style>
