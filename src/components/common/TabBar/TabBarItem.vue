<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="isActive"><slot name="item-icon-active"></slot></div>
    <div v-else><slot name="item-icon"></slot></div>
    <div :class="{ active: isActive }"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  computed: {
    isActive() {
      return this.$route.path == this.path;
    },
  },
  props: {
    path: String,
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path);
    },
  },
};
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  height: 24px;
  width: 24px;
  margin-top: 3px;
  vertical-align: center;
  margin-bottom: 2px;
}
.active {
  color: red;
}
</style>