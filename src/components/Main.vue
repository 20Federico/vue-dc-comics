<template>
  <main>
    <div class="container">
      --> Content goes here &lt;--
    </div>
  </main>
</template>

<script>
export default {
  name: "Main",
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

  main {
    background-color: black;
    padding: $padding_xxlarge 0;

    .container {
      color: white;
      font-size: 24px;
      font-weight: bold;
    }
  }

</style>