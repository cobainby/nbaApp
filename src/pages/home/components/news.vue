<template>
  <div class="news-wrapper">
    <div class="title">
      热门新闻
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of newsList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">
            {{item.newsTitle}}
          </p>
          <p class="item-des">
            {{item.newsDes}}
          </p>
          <button class="item-button">了解更多</button>
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
          imgUrl:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1536991562,3960452145&fm=15&gp=0.jpg",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        },
        {
          id:"02",
          imgUrl:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1536991562,3960452145&fm=15&gp=0.jpg",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        },
        {
          id:"03",
          imgUrl:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1536991562,3960452145&fm=15&gp=0.jpg",
          newsTitle:"nba休赛季交易大盘点",
          newsDes:"签约情况-选秀情况-交易情况(球队动荡新格局)"
        },
        {
          id:"04",
          imgUrl:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1536991562,3960452145&fm=15&gp=0.jpg",
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
  overflow:hidden
  display:flex
  height:1.9rem
  .item-img
    height:1.7rem
    width:1.7rem
    padding:.1rem
  .item-info
    flex:1
    padding:.1rem
    min-width:0
    .item-title
      line-height:.54rem
      font-size:.32rem
      ellipsis()
    .item-des
      line-height:.4rem
      color:#ccc
      ellipsis()
    .item-button
      line-hgiht:.44rem
      margin-top:.2rem
      padding:0 .2rem
      background:#08CFE8
      border-radius:.06rem
      color:#fff
      font-size:0.27rem
</style>
