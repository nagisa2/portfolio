<template>
  <div class="nav-cp">
    <div class="nav-item">
      <div class="nav-link">
        <RouterLink to="/" id="link" class="nav-icon" exact>
          <div class="icon-container">
            <svg class="icon" viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z"
              />
            </svg>
          </div>
        </RouterLink>
        <span>Home</span>
      </div>
      <div class="nav-link">
        <RouterLink to="/about" id="link" class="nav-icon">
          <div class="icon-container">
            <svg class="icon" viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M12,4A4,4 0 0,1 16,8A4,4 0 0,1 12,12A4,4 0 0,1 8,8A4,4 0 0,1 12,4M12,14C16.42,14 20,15.79 20,18V20H4V18C4,15.79 7.58,14 12,14Z"
              />
            </svg>
          </div>
        </RouterLink>
        <span>About</span>
      </div>
      <div class="nav-link">
        <RouterLink to="/portfolio" id="link" class="nav-icon">
          <div class="icon-container">
            <svg class="icon" viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M17,16.47V7.39L11,11.93M2.22,9.19C1.92,8.87 1.91,8.37 2.2,8.04L3.4,6.93C3.6,6.75 4.09,6.67 4.45,6.93L7.87,9.54L15.8,2.29C16.12,1.97 16.67,1.84 17.3,2.17L21.3,4.08C21.66,4.29 22,4.62 22,5.23V18.73C22,19.13 21.71,19.56 21.4,19.73L17,21.83C16.68,21.96 16.08,21.84 15.87,21.63L7.85,14.33L4.45,16.93C4.07,17.19 3.6,17.12 3.4,16.93L2.2,15.83C1.88,15.5 1.92,14.96 2.25,14.63L5.25,11.93"
              />
            </svg>
          </div>
        </RouterLink>
        <span>Portfolio</span>
      </div>
      <div class="nav-link">
        <RouterLink to="/contact" id="link" class="nav-icon">
          <div class="icon-container">
            <svg class="icon" viewBox="0 0 24 24">
              <path
                fill="currentColor"
                d="M20,2H4A2,2 0 0,0 2,4V22L6,18H20A2,2 0 0,0 22,16V4C22,2.89 21.1,2 20,2Z"
              />
            </svg>
          </div>
        </RouterLink>
        <span>Contact</span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>
<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
@import "../style/NavComponent.css";
</style>
