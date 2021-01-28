<template>
  <div class="recommends">
    <div v-for="(item, index) in recommends" :key="index" class="item">
      <a :href="item.link">
        <img :src="item.image" alt="" />
        <p>{{ item.title }}</p>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecommendView",
  props: {
    recommends: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style>
.recommends {
  display: flex;
  margin: 0.5rem 0.375rem 0;
  border-radius: 0.9375rem;
  overflow: hidden;
}
.item {
  flex: 1;
  text-align: center;
  background-color: #fff;
  padding: 0.875rem 0;
}
.item img {
  width: 80%;
  margin-bottom: 0.375rem;
}
</style>