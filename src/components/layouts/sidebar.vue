<template>
  <div id="sidebar">
    <div class="header">
      <img src="@/assets/pays.png" alt="american-flag" class="pays"/>
    </div>

    <div class="my-order-title">
      <h2>My <br>Order</h2>
      <h3>Take Out</h3>
    </div>

    <div class="panier">
      <card-product
        v-for="(item, index) in panier"
        :key="index"
        :item="item"
      />
    </div>

    <div class="validation">
      <span class="separateur"></span>
      <span>Total</span><br>
      <span class="totalPrice">${{ totalPrice }}</span><br>
      <button class="btnDone">Done</button>
    </div>
  </div>
</template>

<script>
import cardProduct from '../card-product'

export default {
  name: "sidebar",
  components: {
    cardProduct,
  },
  props: {
    panier: [],
    totalPrice: Number
  },
}
</script>

<style scoped>

</style>