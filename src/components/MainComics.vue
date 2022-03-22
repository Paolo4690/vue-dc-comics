<template>
  <main>
    <div class="top-main">
      <div class="container">{{ msg }}</div>
    </div>
    <div class="end-main">
      <div class="container">
      </div>
    </div>
  </main>
</template>

<script>

export default {
  name: 'MainComics',
  data () {
    return {
      msg: '-->Content goes here <--'
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
  .container {
    flex: 1 0 100%;
    justify-content: space-between;
  }
}
</style>
