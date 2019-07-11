<template>
  <div class="icons">
    <swiper>
      <!-- slides -->
      <swiper-slide
        v-for="(page,index) of pages"
        :key="index"
      >
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img
              class="icon-img-content"
              :src="item.imgUrl"
            >
          </div>
          <p class="icon-title">{{item.des}}</p>
        </div>
      </swiper-slide>
      <!-- Optional controls -->
      <div
        class="swiper-pagination"
        slot="pagination"
      ></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data() {
    return {
      iconList: [
        {
          id: "001",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          des: "热门新闻"
        },
        {
          id: "002",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          des: "球星轶闻"
        },
        {
          id: "003",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
          des: "nba数据"
        },
        {
          id: "004",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png",
          des: "比赛实录"
        },
        {
          id: "005",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/184e261814a5d07a5d3d08cd29cf590d.png",
          des: "技术分析"
        },
        {
          id: "006",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png",
          des: "球队分区"
        },
        {
          id: "007",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png",
          des: "球迷交流"
        },
        {
          id: "008",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/184e261814a5d07a5d3d08cd29cf590d.png",
          des: "赛后花边"
        },
        {
          id: "009",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png",
          des: "交易流言"
        }
      ]
    };
  },
  computed: {
    pages() {
      const pages = [];
      this.iconList.forEach((item, index) => {
        //当前的icon图标应该在第几页
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';

.icons >>>.swiper-container {
  overflow: hidden;
  height: 0;
  padding-bottom: 50%;
}
.icons
  margin-top:.1rem
  .icon {
    position: relative;
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding: 0.1rem;

      .icon-img-content {
        height: 100%;
        display: block;
        margin: 0 auto;
      }
    }

    .icon-title {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      text-align: center;
      color: $blackTextColor;
      ellipsis();
    }
  }
</style>
