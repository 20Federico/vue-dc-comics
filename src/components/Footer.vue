<template>
  <footer>
    <BannerInfo></BannerInfo>

    <div class="company_more_info">
      <div class="container">
        <div class="info_container">
          <div class="list" v-for="(list, i) in moreInfoLists" :key="i">
            <h3>{{ list.title }}</h3>
            <ul>
              <li v-for="(link, i) in list.links" :key="i"><a :href=" link.href ">{{ link.name }}</a></li>
            </ul>
          </div>
        </div>
        <div class="logo_bg_container"></div>
      </div>
    </div>

    <div class="footer_foot">
      <div class="container">
        <button>SIGN-UP NOW!</button>
        <div>
          <div class="social_container">
            FOLLOW US
            <div class="social_list">
              <a :href=" social.href " v-for="(social, i) in socialList" :key="i">
                <img :src="require('../assets/' + social.imgSrc)" :alt="social.name" >
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

  </footer>
</template>

<script>
  import BannerInfo from './BannerInfo.vue';

  export default {
    name: "Footer",
    components: {
      BannerInfo
    },
    data() {
      return {
        moreInfoLists: [
          {
            title: 'DC COMICS',
            links: [
              {
                name: 'Characters',
                href: '#',
              },
              {
                name: 'Comics',
                href: '#',
              },
              {
                name: 'Movies',
                href: '#',
              },
              {
                name: 'TV',
                href: '#',
              },
              {
                name: 'Games',
                href: '#',
              },
              {
                name: 'Videos',
                href: '#',
              },
              {
                name: 'News',
                href: '#',
              },
            ]
          },
          {
            title: 'SHOP',
            links: [
              {
                name: 'Shop DC',
                href: '#',
              },
              {
                name: 'Shop DC Collectibles',
                href: '#',
              },
            ]
          },
          {
            title: 'DC',
            links: [
              {
                name: 'Terms Of Use',
                href: '#',
              },
              {
                name: 'Privacy policy(New)',
                href: '#',
              },
              {
                name: 'Ad Choices',
                href: '#',
              },
              {
                name: 'Advertising',
                href: '#',
              },
              {
                name: 'Jobs',
                href: '#',
              },
              {
                name: 'Subscriptions',
                href: '#',
              },
              {
                name: 'Talent Workshops',
                href: '#',
              },
              {
                name: 'CPSC Certificates',
                href: '#',
              },
              {
                name: 'Ratings',
                href: '#',
              },
              {
                name: 'Shop Help',
                href: '#',
              },
              {
                name: 'Contact Us',
                href: '#',
              },
            ]
          },
          {
            title: 'SITES',
            links: [
              {
                name: 'DC',
                href: '#',
              },
              {
                name: 'MAD Magazine',
                href: '#',
              },
              {
                name: 'DC Kids',
                href: '#',
              },
              {
                name: 'DC Universe',
                href: '#',
              },
              {
                name: 'DC Power Visa',
                href: '#',
              },
            ]
          },

        ],
        socialList: [
          {
            name: 'facebook',
            href: '#',
            imgSrc: 'footer-facebook.png'
          },
          {
            name: 'twitter',
            href: '#',
            imgSrc: 'footer-twitter.png'
          },
          {
            name: 'youtube',
            href: '#',
            imgSrc: 'footer-youtube.png'
          },
          {
            name: 'pinterest',
            href: '#',
            imgSrc: 'footer-pinterest.png'
          },
          {
            name: 'periscope',
            href: '#',
            imgSrc: 'footer-periscope.png'
          }
        ]
      }
    }
  }
</script>

<style scoped lang="scss">
  @import '../styles/variables';
  
  .company_more_info {
    color: $color_light;
    background-image: url(../assets/footer-bg.jpg);
    background-position: center;
    background-size: cover;

    .container {
      display: flex;
      justify-content: space-between;

        .info_container {
          max-height: 350px;
          display: flex;
          flex-direction: column;
          flex-wrap: wrap;
          align-items: flex-start;
          width: 30%;
          padding: $padding_xlarge 0;

          h3 {
            margin: 0;
          }
          ul {
            list-style: none;
            padding: 0;

            a {
              color: $color_grey;
              text-decoration: none;
            }
          }
        }

        .logo_bg_container {
          width: 45%;
          background-image: url(../assets/dc-logo-bg.png);
          background-position: center;
        }
    }

  }

  .footer_foot {
    background-color: $color_bg_dark;
    padding: $padding_large 0;

    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;

      button {
        color: $color_light;
        background-color: transparent;
        border: 1px solid $color_primary;
        padding: $padding_xsmall $padding_small;
        font-weight: bold;
      }

      .social_container {
        color: $color_primary;
        font-weight: bold;
        margin: 0;
        display: flex;
        align-items: center;
        
        .social_list {
          padding-left: $padding_small;
        }
        img {
          padding: 7px;
        }
      }

    }
  }

</style>