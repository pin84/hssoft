<template>
  <div class="menu">
    <div></div>

    <ul class="list">
      <li
        @click="toPage(item)"
        class="item"
        v-for="(item,index) in menuList"
        :key="index"
      >{{item.name}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuList: [
        { name: "home", router: "/" },
        { name: "关于汉水", router: "/about" },
        { name: "支持服务", router: "/" },
        { name: "联系我们", router: "/" }
      ]
    };
  },

  methods: {
    toPage(item) {
      let { fullPath } = this.$route;
      if (fullPath !== item.router) {
        this.$router.push(item.router);
      }
      this.$emit("closeMenu");
    }
  }
};
</script>

<style lang="stylus" scoped>
.menu
  background-color #000
  color #f5f5f7
  .list
    padding 0 40px
    .item
      padding 15px 0
      border-bottom 1px solid rgb(245, 245, 247);
</style>