<template>
  <div class="home">
    <div class="ad">
      <p>广西汉水软件有限公司</p>
      <p>为您服务</p>
    </div>

    <HomeP1 />
    <HomeP2 />

    <!-- <Footer /> -->
  </div>
</template>

<script>
export default {
  components: {
    HomeP1: () => import("./HomeP1"),
    HomeP2: () => import("./HomeP2"),
    // Footer: () => import("../foot/Footer")
  },

  created() {}
};
</script>

<style lang="stylus" scoped>
.home
  display flex
  flex-direction column
  .ad
    text-align center
    padding 10px

</style>