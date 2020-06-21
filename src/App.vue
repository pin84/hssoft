<template>
  <div id="app">
    <div class="header-box">
      <Header />
    </div>
    <div class="view-box">
      <router-view />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "@/views/header";
import Footer from "@/views/foot/Footer";
export default {
  name: "App",
  components: {
    Header,
    Footer
  }
};
</script>

<style lang="scss">
@import "./style/normalize.scss";
@import "./style/reset.scss";
@import "./style/common.scss";
@import "~@/assets/iconfont/iconfont.css";
#app {
  position: relative;
  font-size: $font-size-base;
  color: $color-common;
  font-family: -apple-system, BlinkMacSystemFont, "PingFang SC", "SF UI Text",
    "Helvetica Neue", STHeiti, "Microsoft Yahei", Tahoma, Simsun, sans-serif;
  height: 100vh;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  .header-box {
    position: absolute;
    width:100%;
    flex: 0 0 50px;
    background-color: none;
  }
  .view-box {
    height: 100%;
    overflow: scroll;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding-top:50px;
  }
}
</style>
