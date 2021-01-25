<template>
  <div class="nav-bar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>
</template>

<script scoped>
export default {
  name: "NavBar",
};
</script>

<style>
.nav-bar {
  width: 100%;
  height: 2.75rem;
  line-height: 2.75rem;
  text-align: center;
  display: flex;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.2);
}
.left,
.right {
  width: 2.75rem;
}
.center {
  flex: 1;
}
</style>