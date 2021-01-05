<template>
  <div>
    <logo></logo>
    <Nav></Nav>
    <div class="flex w">
      <carousel></carousel>
      <fast></fast>
    </div>
    <picmenu></picmenu>
    <div class="flex w">
      <tab></tab>
      <conRight></conRight>
    </div>
    <blogroll></blogroll>
    <footers></footers>
  </div>
</template>

<script>
import logo from "./index_module/logo.vue";
import Nav from "./index_module/Nav.vue";
import carousel from "./index_module/carousel.vue";
import fast from "./index_module/fast.vue";
import picmenu from "./index_module/picmenu.vue";
import tab from "./index_module/tab.vue";
import conRight from "./index_module/conRight.vue";
import blogroll from "./index_module/blogroll.vue";
import footers from "./index_module/footers.vue";

export default {
  name: "App",
  components: {
    logo,
    Nav,
    carousel,
    fast,
    picmenu,
    tab,
    conRight,
    blogroll,
    footers
  }
};
</script>

<style>
.flex {
  display: flex;
  justify-content: space-between;
}
</style>