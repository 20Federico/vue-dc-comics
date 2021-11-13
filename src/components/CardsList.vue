<template>
  <div class="component_container">
    <div class="banner">
    </div>
    <div class="container">
      <div class="label">
        CURRENT SERIES
      </div>
      <div class="cards_box">
        <Card v-for="(cardInfo, i) in cardsInfo" :key="i"
          :card="cardInfo"
        ></Card>
      </div>
      <button class="btn_primary">LOAD MORE</button>
    </div>
  </div>
</template>

<script>
  import Card from '@/components/Card.vue';
  import CardsInfoList from '@/assets/dc-comics.json';

  export default {
    name: "CardsList",
    components: {
      Card,
    },
    data() {
      return {
        cardsInfo: CardsInfoList 
      }
    }
  }
</script>

<style scoped lang="scss">
  @import '../styles/variables';


  .component_container {
    background-color: black;
    height: 100vh;

    .banner {
        height: 35%;
        background-image: url('../assets/jumbotron.jpg');
        background-size: cover;
    }
    .container {
      height: 65%;
      display: flex;
      align-items: center;
      position: relative;

      .label {
        color: $color-light;
        background-color: $color_primary;
        position: absolute;
        top: 0;
        transform: translateY(-50%);
        font-size: 20px;
        font-weight: bold;
        padding: 5px $padding_medium;
      }

      .cards_box {
        width: 100%;
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
      }

      button {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        bottom: $padding_medium;
      }
    }
  }

</style>