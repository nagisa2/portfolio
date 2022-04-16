<template>
<div class="app-container">
  <div class="sidebar">
    <Nav />
  </div>
  <div class="content">
  <router-view />
</div>

  </div>

</template>
<style>
@import "./style/global.css";
</style>
<script setup>
import Nav from "./components/NavComponent.vue";
</script>
