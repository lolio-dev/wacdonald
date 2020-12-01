<template>
  <div id="card-product">
    <img :src="item.icon" alt=""><br>
    <span class="name">{{ item.name }}</span><br>
    <span class="price">{{ item.price }}€</span>

    <div class="quantity">
      <button @click="quantity--">-</button>
      <span class="quantity">{{ quantity }}</span>
      <button @click="quantity++">+</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "card-product",
  props: {
    item: Object,
  },
  data(){
    return {
      quantity: 0,
    }
  }
}
</script>

<style src="../style/card-product.css" />