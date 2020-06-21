<template>
  <div class="footer">
    <p>Copyright © 2020 hssoft Inc. 保留所有权利。</p>
    <p class="policy">
      <span class="text" v-for="(text,index) in textArr" :key="index">{{text}}</span>
    </p>
    <p>
      <span>粤ICP备19021187号</span>
      <span class="bl" @click='checkBusinessLicense'>营业执照</span>
    </p>
    <p></p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      textArr: ["隐私政策", "使用条款", "销售政策", "法律信息", "网站地图"]
    };
  },
  methods:{
    checkBusinessLicense(){
      this.$router.push({name:'businesslicense'})
    }
  }
};
</script>
<style lang="stylus" scoped>
.footer
  background-color #f5f5f7
  color #515154
  padding 10px
  font-size 12px
  p
    margin-bottom 5px
  .policy
    display flex
    padding 5px 0
    .text
      padding 0 8px
      border-left 1px solid rgb(210, 210, 215)
      &:first-child
        padding-left 0
        border-left none
  .bl
    margin-left 10px

</style>