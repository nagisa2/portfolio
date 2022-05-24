<template>
  <div class="portfolio-btn">
    <a :href="`${publicPath}`" download> Download cv </a>
  </div>
</template>

<script>
export default {
  data: () => ({ publicPath: "/public/CollinsOdongoCv.pdf" }),
};
</script>

<style>
@import "../style/DownloadCv.css";
</style>
