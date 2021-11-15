<template>
  <header>
    <nav class="container">
      <img src="../assets/dc-logo.png" alt="dc logo">
      <ul>
        <li v-for="(link, i) in navLinks" :key="i"><a :class="currentIndex === i ? 'active': ''" @click="currentIndex = i" :href="link.href">{{ link.linkName }}</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data(){
    return {

      navLinks: [
        {linkName: 'CHARACTERS', href: '#'},
        {linkName: 'COMICS', href: '#'},
        {linkName: 'MOVIES', href: '#'},
        {linkName: 'TV', href: '#'},
        {linkName: 'GAMES', href: '#'},
        {linkName: 'COLLECTIBLES', href: '#'},
        {linkName: 'VIDEOS', href: '#'},
        {linkName: 'FANS', href: '#'},
        {linkName: 'NEWS', href: '#'},
        {linkName: 'SHOP', href: '#'},
      ],
      currentIndex: 0
    }
  }
}
</script>

<style scoped lang="scss">
@import '../styles/variables';
  

  header {
    position: relative;
  
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: $padding_medium 0;

      img {
        width: 80px;
      }

      ul {
        list-style-type: none;
        display: flex;
        margin: 0;

        a {
          display: inline-block;
          padding: $padding_xsmall $padding_small;
          font-weight: bold;
          text-decoration: none;
          color: $color_dark_grey;
          position: relative;

          &.active {
            color: $color_primary;
            
            &::before {
              content: "";
              width: 100%;
              height: 4px;
              background-color: $color_primary;
              position: absolute;
              bottom: -39px;
              left: 0;
            }
          }
        }
      }
    }
  }
  
</style>