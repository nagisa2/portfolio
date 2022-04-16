<template>
  <div class="nav-container">
    <div class="nav">
      <router-link to="/">
        <img src="../assets/home.svg" alt="home" class="nav-icon" />
      </router-link>
      <router-link to="/about">
        <img src="../assets/about.svg" alt="about" class="nav-icon" />
      </router-link>
      <router-link to="/portfolio">
        <img src="../assets/portfolio.svg" alt="portfolio" class="nav-icon" />
      </router-link>
      <router-link to="/contact">
        <img src="../assets/contact.svg" alt="contact" class="nav-icon" />
      </router-link>
    </div>
  </div>
</template>
<style>
@import "../style/NavComponent.css";
</style>
