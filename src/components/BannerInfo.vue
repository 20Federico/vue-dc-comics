<template>
  <div class="company_info">
    <div class="container">
      <div class="element" v-for="(info, i) in infoList" :key="i">
        <img :src="require('../assets/' + info.imgSrc)" />
        <a :href="info.href">{{ info.title }}</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "BannerInfo",
    data() {
      return {
        infoList: [
          {
            title: 'DIGITAL COMICS',
            imgSrc: 'buy-comics-digital-comics.png',
            href: '#',
          },
          {
            title: 'DC MERCHANDISE',
            imgSrc: 'buy-comics-merchandise.png',
            href: '#',
          },
          {
            title: 'SUBSCRIPTION',
            imgSrc: 'buy-comics-subscriptions.png',
            href: '#',
          },
          {
            title: 'COMIC SHOP LOCATOR',
            imgSrc: 'buy-comics-shop-locator.png',
            href: '#',
          },
          {
            title: 'DC POWER VISA',
            imgSrc: 'buy-dc-power-visa.svg',
            href: '#',
          }
        ],
      }
    }
  }
</script>

<style scoped lang="scss">
  @import '../styles/variables';
  
  .company_info {
    background-color: $color_primary;
    padding: $padding_xxlarge 0;

    .container {
      display: flex;
      justify-content: space-around;
    }
    .element {
      display: flex;
      align-items: center;
    
      img {
        height: 50px;
      }
      a {
        text-decoration: none;
        color: $color_light;
        padding: $padding_xsmall $padding_small;
      }
    }
  }
</style>