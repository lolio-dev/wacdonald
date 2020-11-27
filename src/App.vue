<template>
  <div id="app">

    <div class="menu">
      <header>
        <img src="@/assets/logo.png" alt="logo" class="logo">
      </header>
      <AppMenu v-on:updatePanier="updatePaner($event)"/>
    </div>
    <div class="sidebar">
      <sidebar :panier="Panier"/>
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
      Panier: {},
    }
  },
  methods: {
    updatePaner: function (panier) {
      console.log(panier[0].name)
      console.log(panier)
    }
  }
}
</script>

<style>
@import 'style/main.css';
@import 'style/reset.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&display=swap');
</style>
