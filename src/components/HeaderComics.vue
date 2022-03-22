<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="logo DC" />
      </div>
      <div class="header-menu">
        <ul>
          <li v-for="(item, index) in headerMenu" :key="index" :class="{active: index == activeIndex}">
              <a :href="item.href" :class="{active: index == activeIndex}">{{ item.text }}</a>
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
      activeIndex: 1,
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
@import '../assets/styles/partial/variables';
.logo {
    display: flex;
    align-items: center;
    margin-right: auto;
  img {
    width: 70px;
    height: 70px;
    margin: 10px 0;
  }
}
.header-menu {
  flex-shrink: 0;
  height: 100px;
    ul {
      display: flex;
      align-items: center;
      line-height: 95px;
        li:first-child {
          margin-left: 0;
        }
        li {
          display: inline-block;
          margin-left: 1.2rem;
          border-bottom: 5px solid transparent;
          transition: border-color .25s;
            &:hover,
            &.active {
                border-color: $blu_color;
            }

            a {
              display: inline-block;
              text-decoration: none;
              color: $grey_color;
                &:hover,
                &.active {
                  color: $blu_color;
                }
            }
        }
    }
}

</style>
