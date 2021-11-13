<template>
  <div class="card">
    <div class="cover_box" :style="{ backgroundImage: `url(${card.thumb})` }">
    </div>
    <div class="overlay">
      <p>type: {{ card.type }}</p>
      <p>price: {{ card.price }}</p>
    </div>
    <p>{{card.series.toUpperCase()}}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ['card']
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

  .card {
    width: calc(100% / 6 - 20px);
    padding-bottom: $padding_small;
    color: $color_light;
    font-size: 14px;
    position: relative;

    .cover_box {
      width: 100%;
      aspect-ratio: 1 / 1;
      margin-bottom: $padding_xsmall;
      transition: 0.5s;
    }

    .overlay {
      position: absolute;
      top: 10px;
      left: 10px;
      font-size: 16px;
      font-weight: bold;
      opacity: 0;
      transition: 0.5s;
      transition-delay: 0.2s;
    }

    &:hover {
      .cover_box {
        opacity: 0.2;
      }
      .overlay {
        opacity: 1;
      }
    }
  }
</style>