<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe682;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe63d;</span>输入球星名字</div>
    <div class="header-right">球星<span class="iconfont arrow-icon">&#xe64a;</span></div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader"
};
</script>
<style lang="stylus" scoped>
//注入公共变量，弹性盒子头部分区大
@import '~styles/varibles.styl'

.header
  display: flex
  height: 0.86rem
  line-height: 0.86rem
  color: #fff
  background: $bgColor
  .header-left
    width: 0.64rem
    float: left
    .back-icon
      text-align:center
      font-size:.4rem
  .header-input 
    flex: 1
    height: 0.64rem
    margin-top: 0.12rem
    margin-left: 0.2rem
    background: #fff
    border-radius: 0.1rem
    color: #ccc
    line-height: 0.64rem
    padding-left:.2rem
  .header-right 
    width: 1.24rem
    float: right
    text-align: center
    .arrow-icon
      font-size :.24rem
      margin-left:.1rem
</style>


