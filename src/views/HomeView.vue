<template>
  <div class="home-container">
    <div class="whois">
      <span> -welcome </span>
      <h1>
        {{ whoiam }}
      </h1>
    </div>
    <div class="my-img"></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      whoiam: "Hi,iam collins odongo",
    };
  },

  mounted: {
      
  }
};
</script>

<style>
@import "../style/HomeView.css";
</style>
