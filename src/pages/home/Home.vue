<template>
  <div>
    <home-header :stars='stars'></home-header>
    <home-swiper :list='swiperList'></home-swiper>
    <home-icons :list='iconList'></home-icons>
    <home-news :list='newsList'></home-news>
    <home-teams :list='teamsList'></home-teams>

  </div>
</template>

<script>
import HomeHeader from "./components/Header";
import HomeSwiper from "./components/Swiper";
import HomeIcons from "./components/icons";
import HomeNews from "./components/news";
import HomeTeams from "./components/teams";
import axios from "axios";
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeNews,
    HomeTeams
  },
  data() {
    return {
      stars: "",
      swiperList: [],
      iconList: [],
      newsList: [],
      teamsList: []
    };
  },
  methods: {
    getAllInfo() {
      axios.get("/api/home.json").then(res => {
        debugger;
        if (res.data.result == 0) {
          this.swiperList = res.data.data.swiperList;
          this.iconList = res.data.data.iconList;
          this.newsList = res.data.data.newsList;
          this.teamsList = res.data.data.teamsList;
        }
      });
    }
  },
  mounted() {
    this.getAllInfo();
  },
  
};
</script>
<style>
</style>


