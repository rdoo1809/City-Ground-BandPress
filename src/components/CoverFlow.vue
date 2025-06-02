<script setup>
import {onMounted} from "vue";
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
    <h2>City Ground Originals</h2>
    <div class="carousel">
      <ul>
        <Release :image="CoverOne" link="https://www.youtube.com/watch?v=fagEbM5qvCw"/>
        <Release :image="CoverTwo" link="https://www.youtube.com/watch?v=fagEbM5qvCw"/>
        <Release :image="CoverOne" link="https://www.youtube.com/watch?v=fagEbM5qvCw"/>
      <Release image="/City-Ground-BandPress/images/nkO4szY9iLcgDNuBy10MGctVvxVo4BPywv6TD56X.png" link="https://www.youtube.com/watch?v=wi5czivqM08" />
</ul>
    </div>
  </div>
</template>

<style scoped>
.hero {
  width: 100vw;
}

.hero .carousel {
  width: 300px;
  margin: 50px auto;
  overflow: visible;
}
</style>
