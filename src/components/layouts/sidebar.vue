<template>
  <div id="sidebar">
    <div class="header">
      <img src="@/assets/pays.png" alt="logo" class="pays"/>
    </div>

    <div class="my-order">
      <h2>My <br>Order</h2>
      <h3>Take Out</h3>
      <div class="panier">
        <!-- v-for card-menu -->
      </div>
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
export default {
  name: "sidebar",
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