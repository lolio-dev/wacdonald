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
      <CardProduct

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
    panier: Array
  },
  data(){
    return{
      logoPath: "/home/elie/Documents/dev/web/wacdonald/src/assets/pays.png",
      totalPrice: 18,
    }
  }
}
</script>

<style scoped>

</style>