<template>
  <div id="goods">
    <goods-list-item v-for="(item, id) in goods" :GoodsList="item" :key="id"/>
  </div>
</template>

<script>
import GoodsListItem from './GoodsListItem.vue'

export default {
  name: "GoodsList",
  components: {
    GoodsListItem
  },
  props: {
    goods: {
      type: Array,
      default(){
        return []
      }
    }
  }
}
</script>

<style scoped>
#goods {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 2px;
  }
</style>