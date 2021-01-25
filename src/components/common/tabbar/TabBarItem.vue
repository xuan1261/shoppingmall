<template>
  <div class="tab-bar-item" @click="itemClick" :style="activeStyle">
    <slot name="item-icon"></slot>
    <slot name="item-text"></slot>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: "#1296db",
    },
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1;
    },
    activeStyle() {
      return this.isActive ? { color: this.activeColor } : {};
    },
  },
  methods: {
    itemClick() {
      if (this.path !== this.$route.path) {
        this.$router.replace(this.path);
      }
    },
  },
};
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  font-size: 0.875rem;
  color: #8a8a8a;
}
.iconfont {
  font-size: 1.375rem;
  margin-top: 0.3125rem;
}
</style>