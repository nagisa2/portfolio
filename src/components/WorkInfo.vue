<template>
  <div class="work-wrapper">
    <div class="work-info">
      <svg class="work-icon" viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="M10,17L6.5,13.5L7.91,12.08L10,14.17L15.18,9L16.59,10.41M19.35,10.03C18.67,6.59 15.64,4 12,4C9.11,4 6.6,5.64 5.35,8.03C2.34,8.36 0,10.9 0,14A6,6 0 0,0 6,20H19A5,5 0 0,0 24,15C24,12.36 21.95,10.22 19.35,10.03Z"
        />
      </svg>
      <div class="info-container">
        <vue3-autocounter
          ref="counter"
          :startAmount="0"
          :endAmount="13"
          :duration="3"
          :autoinit="true"
          class="counter-id"
        />
        <h4>Projects completed</h4>
      </div>
    </div>
    <div class="work-info">
      <svg class="work-icon" viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="M18 6V4H20V2H6C4.9 2 4 2.9 4 4V20C4 21.1 4.9 22 6 22H20V20H15.97C17.2 19.09 18 17.64 18 16V11H8V16C8 17.64 8.81 19.09 10.03 20H6V4H8V6C8 6.55 8.45 7 9 7H17C17.55 7 18 6.55 18 6M13 8C13.55 8 14 8.45 14 9S13.55 10 13 10 12 9.55 12 9 12.45 8 13 8Z"
        />
      </svg>
      <div class="info-container">
        <vue3-autocounter
          ref="counter"
          :startAmount="0"
          :endAmount="4530"
          :duration="3"
          :autoinit="true"
          class="counter-id"
        />
        <h4>Cups of coffee <span class="hide">consumed </span></h4>
      </div>
    </div>
    <div class="work-info">
      <svg class="work-icon" viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="M16 17V19H2V17S2 13 9 13 16 17 16 17M12.5 7.5A3.5 3.5 0 1 0 9 11A3.5 3.5 0 0 0 12.5 7.5M15.94 13A5.32 5.32 0 0 1 18 17V19H22V17S22 13.37 15.94 13M15 4A3.39 3.39 0 0 0 13.07 4.59A5 5 0 0 1 13.07 10.41A3.39 3.39 0 0 0 15 11A3.5 3.5 0 0 0 15 4Z"
        />
      </svg>
      <div class="info-container">
        <vue3-autocounter
          ref="counter"
          :startAmount="0"
          :endAmount="10"
          :duration="3"
          :autoinit="true"
          class="counter-id"
        />
        <h4>Satisfied clients</h4>
      </div>
    </div>
    <div class="work-info">
      <svg class="work-icon" viewBox="0 0 24 24">
        <path
          fill="currentColor"
          d="M17,16.47V7.39L11,11.93M2.22,9.19C1.92,8.87 1.91,8.37 2.2,8.04L3.4,6.93C3.6,6.75 4.09,6.67 4.45,6.93L7.87,9.54L15.8,2.29C16.12,1.97 16.67,1.84 17.3,2.17L21.3,4.08C21.66,4.29 22,4.62 22,5.23V18.73C22,19.13 21.71,19.56 21.4,19.73L17,21.83C16.68,21.96 16.08,21.84 15.87,21.63L7.85,14.33L4.45,16.93C4.07,17.19 3.6,17.12 3.4,16.93L2.2,15.83C1.88,15.5 1.92,14.96 2.25,14.63L5.25,11.93"
        />
      </svg>
      <div class="info-container">
        <vue3-autocounter
          ref="counter"
          :startAmount="0"
          :endAmount="8"
          :duration="3"
          :autoinit="true"
          class="counter-id"
        />
        <h4>upcoming projects</h4>
      </div>
    </div>
  </div>
</template>

<script>
import counter from "vue3-autocounter";
export default {
  components: {
    "vue3-autocounter": counter,
  },
  data() {
    return {};
  },
};
</script>
<style>
@import "../style/WorkInfo.css";
</style>
