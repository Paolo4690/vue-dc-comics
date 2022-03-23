<template>
  <div class="top-main">
    <div class="container">
      <div class="btn-blu-before">current series</div>
      <div class="container-books">
        <CardMain  v-for="item in arrBooks"
          :key="item.series"
          :book-img="item.thumb"
          :book-title="item.series"
        />
      </div>
      <div class="btn-blu-after">Load More</div>
    </div>
  </div>
</template>

<script>
import CardMain from './CardMain.vue'

export default {
  name: 'TopMain',
  components: {
    CardMain
  },
  props: {
    arrBooks: Array
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partial/variables';
.top-main {
  display: flex;
  background-color: #1c1c1c;
  font-size: 1.3rem;
  font-weight: bold;
  padding-bottom: 1rem;
  .container {
    position: relative;
    flex-wrap: wrap;
    justify-content: center;
    .btn-blu-before {
      position: absolute;
      top: -18px;
      left: 0;
      width: 160px;
      height: 35px;
      background-color: $blu_color;
      line-height: 35px;
      text-align: center;
      font-size: 1rem;
      font-weight: 500;
      text-transform: uppercase;
      cursor: pointer;
    }
    .container-books {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      padding: 2rem 0 1rem;
    }
    .btn-blu-after {
      width: 160px;
      height: 35px;
      background-color: $blu_color;
      line-height: 35px;
      text-align: center;
      font-size: .9rem;
      font-weight: 400;
      text-transform: uppercase;
      cursor: pointer;
    }
  }
}
</style>
