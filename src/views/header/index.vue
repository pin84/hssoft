<template>
  <div class="header-wrapper">
    <header>
      <i class="iconfont" :class="isScale ? 'icon-caidan': 'icon-cha1'" @click="showMenu"></i>
      <i style="color:red;" class="iconfont icon-logo"></i>
      <i class="iconfont icon-lock"></i>
    </header>

    <div class="menu" :class="{'isScale':isScale}">
      <Menu />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isScale: false
    };
  },

  components: {
    Menu: () => import("./Menu")
  },
  methods: {
    showMenu() {
      this.isScale = !this.isScale;
    }
  }
};
</script>
<style lang="stylus" scoped>
.header-wrapper
  position relative
  width 100%
  header
    position relative
    padding 0 20px
    height 50px
    display flex
    align-items center
    justify-content space-between
    background-color rgba(0,0,0,0.9)
    z-index 2
    .iconfont
      font-size 24px
      color #fff
  .menu
    position absolute
    width 100%
    height 100vh
    left 0
    top 0
    box-sizing border-box
    padding-top 50px
    transition 1s
    transform-origin  center top
    transform scaleY(1)
    &.isScale
      transform scaleY(0)
</style>