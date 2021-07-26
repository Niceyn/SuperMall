<template>
  <div class="goods">
    <goods-list-item class="goods-info" v-for="item,index in goods" :key='index' :goodsItem="goods[index]"/>
  </div>
</template>

<script>
import GoodsListItem from './GoodsListItem.vue'

export default {
  components:{
    GoodsListItem
  },
  props:{
    goods:{
      type:Array,
      default() {
        return[]
      }
    }
  }
}
</script>

<style>
  .goods{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  /*.goods-info{
    width: 150px;
  }*/
</style>