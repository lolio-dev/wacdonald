<template>
  <div class="Appmenu">
    <div class="MenuTitle">
      <h2 class="Hey">Hey, </h2>
      <h3 class="Wats">Wat's up?</h3>
    </div>

    <div class="FoodContainer">
      <div
          class="FoodItem"
          v-for="menu in menu"
          :key="menu"
          @click="add(menu)"
      >
        <img :src="menu.icon" alt="">
        <span>{{ menu.name }}</span>
        <span>{{ menu.price }}$</span>
      </div>
    </div>
  </div>
</template>

<script>
import menu from '@/menu.json'

export default {
  name: "AppMenu",
  data(){
    return {
      menu,
    }
  },
  methods: {
    add(item){
      this.$emit('updatePanier', item)
    }
  }
}
</script>

<style scoped>

</style>