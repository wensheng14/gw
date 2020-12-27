<template>
  <div id="app">
    <logo></logo>
    <Nav></Nav>
    <div class="lunbo w">
      <carousel></carousel>
      <fast></fast>
    </div>
  </div>
</template>

<script>
import logo from './components/logo.vue'
import Nav from './components/Nav.vue'
import carousel from './components/carousel.vue'
import fast from './components/fast.vue'

export default {
  name: 'App',
  components: {
    logo,
    Nav,
    carousel,
    fast,
  }
}
</script>

<style>
.lunbo {
  display: flex;
  justify-content: space-between;
}
</style>
