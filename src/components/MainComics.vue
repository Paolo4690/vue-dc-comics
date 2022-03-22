<template>
  <main>
    <div class="top-main">
      <div class="container">{{ msg }}</div>
    </div>
    <div class="end-main">
      <div class="container">
        <div v-for="(card, index) in cardsEndMain" :key="index" class="content-card">
          <img :src="card.img" :alt="card.text">
          <span>{{ card.text }}</span>
        </div>
      </div>
    </div>
  </main>
</template>

<script>

export default {
  name: 'MainComics',
  data () {
    return {
      msg: '-->Content goes here <--',
      cardsEndMain: [
        {
          img: '../assets/img/buy-comics-digital-comics.png',
          text: 'digitals comics'
        },
        {
          img: '../assets/img/buy-comics-merchandise.png',
          text: 'dc merchandise'
        },
        {
          img: '../assets/img/buy-comics-subscriptions.png',
          text: 'subscription'
        },
        {
          img: '../assets/img/buy-comics-shop-locator.png',
          text: 'comic shop locator'
        },
        {
          img: '../assets/img/buy-dc-power-visa.svg',
          text: 'dc power visa'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partial/variables';
.top-main {
  display: flex;
  height: 100px;
  background-color: #1c1c1c;
  font-size: 1.3rem;
  font-weight: bold;
  .container {
    flex: 1 0 100%;
  }
}
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
        width: 20%;
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
