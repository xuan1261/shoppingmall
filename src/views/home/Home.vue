<template>
  <div class="home">
    <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
    <my-swiper :banners="banners" />
    <recommend-view :recommends="recommends" />
    <div class="box"></div>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
import MySwiper from "components/common/swiper/MySwiper";
import RecommendView from "./childComps/RecommendView";

import { getHomeMultidata } from "network/home";

export default {
  name: "Home",
  components: {
    NavBar,
    MySwiper,
    RecommendView,
  },
  data() {
    return {
      banners: [],
      recommends: [],
    };
  },
  created() {
    getHomeMultidata().then((res) => {
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    });
  },
};
</script>

<style>
.home {
  background-color: #f3f3f3;
  padding: 2.75rem 0;
}
.home-nav {
  background-color: #ff8d97;
  color: #fff;
  font-size: 1.5rem;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 99;
}
.box {
  width: 20px;
  height: 1000px;
}
</style>