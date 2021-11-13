<template>
  <main>
    <div class="banner">

    </div>
    <div class="container">
      <Cards-List v-for="(cardInfo, i) in cardsInfo" :key="i"
        :card="cardInfo"
      ></Cards-List>
    </div>
  </main>
</template>

<script>
  import CardsList from '@/components/CardsList.vue';
  import CardsInfoList from '@/assets/dc-comics.json';

  export default {
    name: "Main",
    components: {
      CardsList,
    },
    data() {
      return {
        cardsInfo: CardsInfoList 
      }
    },
    mounted() {
    }
  }
</script>

<style scoped lang="scss">
  @import '../styles/variables';


  main {
    background-color: black;
    height: 100vh;
    .banner {
        height: 35%;
        background-image: url('../assets/jumbotron.jpg');
        background-size: cover;
    }
    .container {
      height: 65%;
      // padding: $padding_xxlarge 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
    }
  }

</style>