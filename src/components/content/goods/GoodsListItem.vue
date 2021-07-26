<template>
  <div class="goods-item">
    <img :src="goodsItem.show.img" alt="" />
    <div class="goods-item-decri">
      <p>{{ goodsItem.title }}</p>
      <span class="price">{{ goodsItem.price }}</span>
      <span class="collect">{{ goodsItem.cfav }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    goodsItem: {
      type: Object,
      default() {
        return [];
      },
    },
  },
  created() {},
};
</script>

<style>
.goods-item {
  font-size: 12px;
  text-align: center;
  padding-bottom: 10px;
  width: 48%;
}
.goods-item img {
  border-radius: 5px;
  width: 100%;
}
.goods-item-decri{
  padding-top: 6px;
}
.goods-item-decri p {
  width: 100%;

  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  padding-bottom:5px ;
}
.goods-item-decri .price {
  color: var(--color-high-text);
}
.goods-item-decri .collect::before {
  position:relative;
  bottom: -2px;
  content: "";
  display: inline-block;
  width: 14px;
  height: 14px;
  background: url("~assets/img/common/collect.svg") 0 0/14px 14px;
}
</style>