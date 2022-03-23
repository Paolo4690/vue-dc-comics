<template>
  <div class="end-main">
    <div class="container">
      <div v-for="(card, index) in arrEndMain" :key="index" class="content-card">
        <img :src="card.img" :alt="card.text">
        <span>{{ card.text }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EndMain',
  props: {
    arrEndMain: Array
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/styles/partial/variables';
.end-main {
  display: flex;
  height: 100px;
  background-color: $blu_color;
  font-size: 1.3rem;
  font-weight: bold;
  text-transform: uppercase;
  .container {
    flex: 1 0 100%;
    justify-content: space-between;
    .content-card {
      display: flex;
      justify-content: center;
      align-items: center;
      width: calc(100% / 5);
      img {
        width: 40px;
      }
      span {
        padding-left: .3rem;
        font-size: .8rem;
        font-weight: normal;
      }
    }
  }
}
</style>
