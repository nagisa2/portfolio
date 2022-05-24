<template>
  <div class="app-c">
    <div class="app-nav">
      <Nav />
    </div>
    <div class="app-content">
      <RouterView />
    </div>
  </div>
</template>

<script>
import { RouterView } from "vue-router";
import AboutView from "./views/AboutView.vue";
import Nav from "./components/NavComponent.vue";
export default {
  components: {
    Nav,
    RouterView,
    AboutView,
  },
};
</script>

<style>
@import "./style/global.css";
</style>
