<template>
  <div id="app">

    <div class="menu">
      <header>
        <img src="@/assets/logo.png" alt="logo" class="logo">
      </header>
      <AppMenu />
    </div>
    <div class="sidebar">
      <sidebar />
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

    }
  }
}
</script>

<style>
@import 'style/main.css';
@import 'style/reset.css';
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&display=swap');
</style>
