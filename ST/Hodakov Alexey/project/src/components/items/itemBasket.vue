<template>
  <div class="d-flex headerCartWrapIn mb-1 p-2">
    <img :src="item.productImg" alt width="85" height="100" />
    <div>
      <div>{{item.productName}}</div>
      <span>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star-half-alt"></i>
      </span>
      <div class="headerCartWrapPrice">
        {{item.amount}}
        <span>x</span>
        ${{item.productPrice}}
      </div>
    </div>
    <button class="fas fa-times-circle" name="remove"></button>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: () => ({ productName: "NAME", productPrice: 0 }),
    },
  },
  // methods: {
  //   removeBasketItem(item) {
  //     if (item.amount > 1) {
  //       item.amount--;
  //     } else {
  //       this.basketItems.splice(this.basketItems.indexOf(this.find(item)), 1);
  //     }
  //   },
  // },
};
</script>

<style>
</style>