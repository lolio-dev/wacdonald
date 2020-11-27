<template>
  <div>
    <span>{{ name }}</span><br>
    <span>{{ price }}€</span>
  </div>
</template>

<script>
export default {
  name: "card-product",
  props: {
    name: String,
    price: Number,
  }
}
</script>

<style scoped>

</style>