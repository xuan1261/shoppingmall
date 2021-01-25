<template>
  <tab-bar>
    <tab-bar-item path="/home">
      <div slot="item-icon" class="iconfont icon-shouye1"></div>
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <div slot="item-icon" class="iconfont icon-fenlei"></div>
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <div slot="item-icon" class="iconfont icon-ziyuan"></div>
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <div slot="item-icon" class="iconfont icon-wode"></div>
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
import TabBar from "components/common/tabbar/TabBar";
import TabBarItem from "components/common/tabbar/TabBarItem";

export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem,
  },
};
</script>

<style>
</style>