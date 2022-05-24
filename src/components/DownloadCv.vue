<template>
  <div class="portfolio-btn" ref="download">
    <a :href="publicPath" download ref="downloadLink"> Download cv </a>
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
