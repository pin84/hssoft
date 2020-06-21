<template>
  <div class="menu">
    <div></div>

    <ul class="list">
      <li class="item" v-for="(item,index) in menuList" :key="index">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuList: ["技术支持", "技术支持", "技术支持", "技术支持", "技术支持"]
    };
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