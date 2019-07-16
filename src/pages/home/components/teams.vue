<template>
  <div class="teams-wrapper">
    <div class="title">
      球队专区
    </div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img
            class="item-img"
            :src="item.imgUrl"
          />
        </div>
        <div class="item-info">
          <p class="item-title">
            {{item.teamsTitle}}
          </p>
          <p class="item-des">
            {{item.teamsDes}}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name:'hometeams',
  props:[
    "list"
  ],
  data(){
    return{
    }
  }

};
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  line-height: 0.8rem;
  text-indent: 0.2rem;
  background: #eee;
}

.item {
  .item-img-wrapper {
    overflow: hidden;
    height: 0;
    padding-bottom: 43.9%;

    .item-img {
      width: 100%;
    }
  }

  .item-info {
    padding: 0.1rem;

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
  }
}
</style>
