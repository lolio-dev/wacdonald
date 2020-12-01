<template>
  <div id="app">

    <div class="menu">
      <header>
        <img src="@/assets/logo.png" alt="logo" class="logo">
      </header>
      <AppMenu v-on:updatePanier="addItem($event)"/>
    </div>
    <div class="sidebar">
      <sidebar
          :panier="panier"
          :total-price="totalPrice"
      />
    </div>
  </div>
</template>

<script>
import sidebar from "./components/layouts/sidebar"
import AppMenu from "@/components/layouts/AppMenu";

export default {
  name: 'App',
  components: {
    sidebar,
    AppMenu
  },
  data(){
    return{
      panier: [],
      totalPrice: 0,
    }
  },
  methods: {
    addItem: function (item) {
      this.totalPrice += item.price
      this.panier.push(item)
    }
  }
}
</script>

<style>
@import 'style/main.css';
@import 'style/reset.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&display=swap');
</style>
