<template>
  <div class="card">
    <div class="cover_box">
    </div>
  </div>
</template>

<script>
export default {
  name: "CardsList",
  props: ['card']
}
</script>

<style scoped lang="scss">
  .card {
    width: calc(100% / 6 - 7px);
    height: 150px;
    .cover_box {
      width: 100%;
      aspect-ratio: 1 / 1;
      // background-image: url('card.thumb')
    }
  }
</style>