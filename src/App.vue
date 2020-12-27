<template>
  <div id="app">
    <logo></logo>
    <Nav></Nav>
    <div class="w">
      <carousel></carousel>
    </div>
  </div>
</template>

<script>
import logo from './components/logo.vue'
import Nav from './components/Nav.vue'
import carousel from './components/carousel.vue'

export default {
  name: 'App',
  components: {
    logo,
    Nav,
    carousel,
  }
}
</script>

<style>
</style>
