<template>
  <div class="home">
    <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";

export default {
  name: "Home",
  components: {
    NavBar,
  },
};
</script>

<style>
.home-nav {
  background-color: #ff8d97;
  color: #fff;
  font-size: 1.5rem;
}
</style>