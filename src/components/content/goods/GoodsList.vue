<template>
  <div class="goods">
    <goods-list-item v-for="item in goods" :goods-item="item" :key="item.index">
    </goods-list-item>
  </div>
</template>

<script>
import GoodsListItem from "./GoodsListItem.vue";

export default {
  props: {
    data() {
      return {
        goods: {
          type: Array,
          default() {
            return [];
          },
        },
      };
    },
  },
  components: {
    GoodsListItem,
  },
};
</script>

<style>
.goods {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;

  padding: 2px;
}
</style>