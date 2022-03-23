<template>
  <div class="content-book">
    <img :src="bookImg" alt="bookTitle">
    <h6>{{ bookTitle }}</h6>
  </div>
</template>

<script>
export default {
  name: 'CardMain',
  props: {
    bookImg: String,
    bookTitle: String
  }
}
</script>

<style scoped lang="scss">
.content-book {
  flex: 0 0 calc(100% / 6 - .8rem);
  margin: 1rem 0;
    img {
    width: 100%;
    height: 160px;
    object-fit: cover;
    object-position: top;
  }
  h6 {
    padding-top: .5rem;
    text-transform: uppercase;
    font-weight: 400;
  }
}

</style>
