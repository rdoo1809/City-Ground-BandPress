<script setup>
import { onMounted } from "vue";
import Release from "./Release.vue";
import CoverOne from "/public/images/cover_one.jpeg"
import CoverTwo from "/public/images/cover_two.jpeg"

onMounted(() => {
  const $ = window.jQuery;
  $(".carousel").flipster({
    style: "carousel",
    spacing: -0.3,
  });
});
</script>

<template>
  <div class="hero">
    <div class="carousel">
      <ul>
        <Release :image="CoverOne" link="https://www.youtube.com/watch?v=fagEbM5qvCw" />
        <Release :image="CoverTwo" link="https://www.youtube.com/watch?v=fagEbM5qvCw" />
        <Release :image="CoverOne" link="https://www.youtube.com/watch?v=fagEbM5qvCw" />
      </ul>
    </div>
  </div>
</template>

<style scoped>
.hero {
  width: 100%;
}
.hero .carousel {
  width: 300px;
  margin: 100px auto;
  overflow: visible;
}
</style>
