<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide
        v-for="item of swiperList"
        :key="item.id"
      >
        <img
          class="swiper-img"
          :src="item.imgUrl"
        />
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
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop:true
      },
      swiperList: [
        {
          id: "001",
          imgUrl:
            "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561655165438&di=741cc9bbc69755469420577bbc1584ef&imgtype=0&src=http%3A%2F%2F04.imgmini.eastday.com%2Fmobile%2F20180608%2F20180608_1a5bb4ec7f4f167dc64e214ec2c174a9_wmk.jpeg"
        },
        {
          id: "002",
          imgUrl:
            "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561653310929&di=fd177bace623d4fcf257a145ab29fc91&imgtype=0&src=http%3A%2F%2Fpic.8win.com%2Fattached%2Fimage%2F20150607%2F20150607101123_761.jpg"
        },
        {
          id: "003",
          imgUrl:
            "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1562250005&di=99e922eb41dc7b0d9102d838f7302abe&imgtype=jpg&er=1&src=http%3A%2F%2F04.imgmini.eastday.com%2Fmobile%2F20180419%2Fc1634063cb3e01f9925764f39a181c23.jpeg"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.wrapper>>>.swiper-pagination-bullet-active {
  background: #fff !important;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 56.25%;
  background: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>
