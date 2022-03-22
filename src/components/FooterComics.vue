<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <div class="footer-top-left">
          <section>
            <ul>
              <li><h3>DC COMICS</h3></li>
              <li v-for="(linkComics, index) in footerLinkComics" :key="index"><a :href="linkComics.href">{{ linkComics.text }}</a></li>
            </ul>
            <ul>
              <li><h3>SHOP</h3></li>
              <li v-for="(linkShop, index) in footerLinkShop" :key="index"><a :href="linkShop.href">{{ linkShop.text }}</a></li>
            </ul>
          </section>
          <section>
            <ul>
              <li><h3>DC</h3></li>
              <li v-for="(linkDc, index) in footerLinkDc" :key="index"><a :href="linkDc.href">{{ linkDc.text }}</a></li>
            </ul>
          </section>
          <section>
            <ul>
              <li><h3>SITES</h3></li>
              <li v-for="(linkSites, index) in footerLinkSites" :key="index"><a :href="linkSites.href">{{ linkSites.text }}</a></li>
            </ul>
          </section>
        </div>
        <div class="footer-top-right"></div>
      </div>
    </div>
    <div class="footer-social">
      <div class="container"></div>
    </div>
  </footer>

</template>

<script>
export default {
  name: 'FooterComics',
  data () {
    return {
      footerLinkComics: [
        {
          href: '#',
          text: 'Characters'
        },
        {
          href: '#',
          text: 'Comics'
        },
        {
          href: '#',
          text: 'Movie'
        },
        {
          href: '#',
          text: 'Tv'
        },
        {
          href: '#',
          text: 'Games'
        },
        {
          href: '#',
          text: 'Videos'
        },
        {
          href: '#',
          text: 'News'
        }
      ],
      footerLinkShop: [
        {
          href: '#',
          text: 'Shop DC'
        },
        {
          href: '#',
          text: 'Shop DC Collectibles'
        }
      ],
      footerLinkDc: [
        {
          href: '#',
          text: 'Terms Of Use'
        },
        {
          href: '#',
          text: 'Privacy policy (New)'
        },
        {
          href: '#',
          text: 'Ad Choices'
        },
        {
          href: '#',
          text: 'Advertising'
        },
        {
          href: '#',
          text: 'Jobs'
        },
        {
          href: '#',
          text: 'Subscriptions'
        },
        {
          href: '#',
          text: 'Talent Workshops'
        },
        {
          href: '#',
          text: 'CPSC Certificates'
        },
        {
          href: '#',
          text: 'Ratings'
        },
        {
          href: '#',
          text: 'Shop Help'
        },
        {
          href: '#',
          text: 'Contact Us'
        }
      ],
      footerLinkSites: [
        {
          href: '#',
          text: 'DC'
        },
        {
          href: '#',
          text: 'MAD Magazine'
        },
        {
          href: '#',
          text: 'DC Kids'
        },
        {
          href: '#',
          text: 'DC Universe'
        },
        {
          href: '#',
          text: 'DC Power Visa'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partial/variables';
.footer-top {
  background-image: url('../assets/img/footer-bg.jpg');
  background-position: center top;
  background-size: cover;
  background-repeat: no-repeat;
  .container {
    justify-content: space-between;
    align-items: stretch;
    .footer-top-left {
      display: flex;
      align-items: flex-start;
      padding: 1.5rem 0 2.5rem ;
      section {
        padding-right: 1rem;
        ul {
          list-style: none;
          a {
            text-decoration: none;
            font-weight: 500;
            color: $grey_color_footer;
            font-size: .9rem;
            transition: color .25s;
            &:hover{
              color: #fff;
            }
          }
          h3 {
            padding: 1rem 0;
            color: #fff;
          }
        }
      }
    }
  }
  .footer-top-right{
    flex: 0 0 45%;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-size: cover;
  }
}
</style>
