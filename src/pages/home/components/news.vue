<template>
  <div class="news-wrapper">
    <div class="title">
      热门新闻
    </div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
      >
        <img
          class="item-img"
          :src="item.imgUrl"
        />
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
  name: "homeNews",
  props: ["list"],
  data() {
    return {};
  }
};
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  text-indent: 0.2rem;
  background: #eee;
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;

  .item-img {
    height: 1.7rem;
    width: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
    padding: 0.1rem;
    min-width: 0;

    .item-title {
      line-height: 0.54rem;
      font-size: 0.32rem;
      ellipsis();
    }

    .item-des {
      line-height: 0.4rem;
      color: #ccc;
      ellipsis();
    }

    .item-button {
      line-hgiht: 0.44rem;
      margin-top: 0.2rem;
      padding: 0 0.2rem;
      background: #08CFE8;
      border-radius: 0.06rem;
      color: #fff;
      font-size: 0.27rem;
    }
  }
}
</style>
