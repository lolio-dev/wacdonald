<template>
  <div id="app">
    <h1>Wac donald</h1>
    <sidebar />
    <menu />
  </div>
</template>

<script>
import sidebar from "./components/layouts/sidebar"
import menu from "./components/layouts/menu"

export default {
  name: 'App',
  components: {
    sidebar,
    // eslint-disable-next-line vue/no-unused-components
    menu
  }
}
</script>

<style>
@import 'style/main.css';
</style>
