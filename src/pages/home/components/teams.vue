<template>
  <div class="news-wrapper">
    <div class="title">
      球队专区
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of newsList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">
            {{item.newsTitle}}
          </p>
          <p class="item-des">
            {{item.newsDes}}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name:'homeNews',
  data(){
    return{
      newsList:[
        {
          id:"01",
          imgUrl:"https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1563205677424&di=73c24eb9604434167e5035ff395d58a4&imgtype=jpg&src=http%3A%2F%2Fimg.mp.itc.cn%2Fupload%2F20170224%2F902b8402938943648d14af0307a0a51e_th.jpeg",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        },
        {
          id:"02",
          imgUrl:"https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1563205912320&di=e3fe91c0c01dfe9809ce0833052b8d2d&imgtype=0&src=http%3A%2F%2F04.imgmini.eastday.com%2Fmobile%2F20170825%2F20170825065301_3b97db2a0005fd37aa15dd720ae1e2a7_1.jpeg",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        },
        {
          id:"03",
          imgUrl:"https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1563205725557&di=4614521d89a142d1deb8b82a7e71a52f&imgtype=0&src=http%3A%2F%2Fsports.cctv.com%2F20081109%2Fimages%2F1226189557164_1226187170621_21163.gif",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        },
        {
          id:"04",
          imgUrl:"https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1563205858949&di=1dd85cf6395e7f4f9e766aa6e37c5c01&imgtype=jpg&src=http%3A%2F%2F5b0988e595225.cdn.sohucs.com%2Fimages%2F20180203%2Ffd34066c905d45c899ad7146ac99c7c7.jpeg",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        }
      ]
    }
  }

};
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';
.title
  margin-top: 0.2rem;
  line-height: 0.8rem;
  text-indent: 0.2rem;
  background: #eee;
.item
  .item-img-wrapper
    overflow:hidden
    height:0
    padding-bottom:43.9%
    .item-img
      width:100%
  .item-info
    padding:.1rem
    .item-title
      line-height:.54rem
      font-size:.32rem
      ellipsis()
    .item-des
      line-height:.4rem
      color:#ccc
      ellipsis()
</style>
