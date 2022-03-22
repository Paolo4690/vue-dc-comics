<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="" />
      </div>
      <div class="header-menu">
        <ul>
          <li v-for="(item, index) in headerMenu" :key="index">
              <a :href="item.href">{{ item.text }}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComics',
  data () {
    return {
      headerMenu: [
        {
          href: '#',
          text: 'characters'
        },
        {
          href: '#',
          text: 'comics'
        },
        {
          href: '#',
          text: 'movie'
        },
        {
          href: '#',
          text: 'tv'
        },
        {
          href: '#',
          text: 'games'
        },
        {
          href: '#',
          text: 'collectibles'
        },
        {
          href: '#',
          text: 'videos'
        },
        {
          href: '#',
          text: 'fans'
        },
        {
          href: '#',
          text: 'news'
        },
        {
          href: '#',
          text: 'shop'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.logo {
  margin-right: auto;
  img {
    width: 60px;
    height: 60px;
    margin: 10px 0;
  }
}

li {
    display: inline-block;
    a {
        display: inline-block;
        text-decoration: none;
    }
}
</style>
