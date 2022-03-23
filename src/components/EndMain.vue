<template>
  <div class="end-main">
    <div class="container">
      <div v-for="(card, index) in arrSectionBlu" :key="index" class="content-card">
        <img :src="card.img" :alt="card.text">
        <span>{{ card.text }}</span>
      </div>
    </div>
  </div>
</template>

<script>
import card1 from '../assets/img/buy-comics-digital-comics.png'
import card2 from '../assets/img/buy-comics-merchandise.png'
import card3 from '../assets/img/buy-comics-subscriptions.png'
import card4 from '../assets/img/buy-comics-shop-locator.png'
import card5 from '../assets/img/buy-dc-power-visa.svg'

export default {
  name: 'EndMain',
  data () {
    return {
      arrSectionBlu: [
        {
          img: card1,
          text: 'digitals comics'
        },
        {
          img: card2,
          text: 'dc merchandise'
        },
        {
          img: card3,
          text: 'subscription'
        },
        {
          img: card4,
          text: 'comic shop locator'
        },
        {
          img: card5,
          text: 'dc power visa'
        }
      ]
    }
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
