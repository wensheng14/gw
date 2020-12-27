<template>
  <div id="app">
    <logo></logo>
    <Nav></Nav>
  </div>
</template>

<script>
import logo from './components/logo.vue'
import Nav from './components/Nav.vue'

export default {
  name: 'App',
  components: {
    logo,
    Nav,
  }
}
</script>

<style>
</style>
